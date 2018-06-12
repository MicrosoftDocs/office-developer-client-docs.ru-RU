---
title: Разработка службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 04aa4348560396c8237811252fd96a2b461cd791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808276"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="df26f-103">Разработка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="df26f-103">Designing a message service</span></span>

<span data-ttu-id="df26f-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df26f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df26f-105">Прежде чем начать писать код для поддержки службы сообщений, важно для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="df26f-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="df26f-106">Устранение следующих проблем в процессе разработки.</span><span class="sxs-lookup"><span data-stu-id="df26f-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="df26f-107">Определите, сколько поставщиков услуг должно быть включено в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="df26f-108">Включите только поставщиков услуг, связанных с ними (поставщиков, которые работают с той же системе обмена сообщениями) в службе.</span><span class="sxs-lookup"><span data-stu-id="df26f-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="df26f-109">Поставщики услуг несвязанных не принадлежат одной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="df26f-110">Используйте профиль по интеграции поставщиков несвязанных службы и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="df26f-111">Определите, какой тип поставщиков услуг должно быть включено в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="df26f-112">Большинство служб сообщения включают одного поставщика каждого из типов.</span><span class="sxs-lookup"><span data-stu-id="df26f-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="df26f-113">То есть служба Типичное сообщение имеет один адресной книге, поставщик хранения одного сообщения и один транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="df26f-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="df26f-114">Определить, сколько библиотек DLL должен содержать службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="df26f-115">Число библиотек DLL, которые использует служба сообщений зависит от следующих:</span><span class="sxs-lookup"><span data-stu-id="df26f-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="df26f-116">Степень сложности, который разработчику службы сообщений требуется для обработки.</span><span class="sxs-lookup"><span data-stu-id="df26f-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="df26f-117">Тип поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="df26f-118">Связь, службы сообщение может быть с другой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="df26f-119">Так как MAPI сохраняет только одну точку входа для каждого типа поставщика, не включают нескольких поставщиков одного типа в одной библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="df26f-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="df26f-120">Если это имеет смысл включать несколько поставщиков одного типа, их реализации в отдельные библиотеки DLL или их совместно использовать функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="df26f-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="df26f-121">Можно реализовать службы сообщений или службы сообщений, которые можно использовать же установки и настройки кода и же DLL точка входа функции, в одной библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="df26f-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="df26f-122">Если это возможно можно проще и используйте один DLL, которая содержит реализации всех поставщиков услуг службы сообщений и весь код для установки и настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="df26f-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="df26f-123">Если это невозможно, можно реализовать один DLL-Библиотеку кода установки и настройки, а также одной библиотеки DLL для всех поставщиков услуг или один DLL-Библиотеку для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="df26f-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="df26f-124">Определите имя службы сообщений DLL или DLL-библиотеки.</span><span class="sxs-lookup"><span data-stu-id="df26f-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="df26f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="df26f-125">See also</span></span>

- [<span data-ttu-id="df26f-126">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="df26f-126">Message Service Implementation</span></span>](message-service-implementation.md)

