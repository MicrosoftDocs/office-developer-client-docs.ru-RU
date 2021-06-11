---
title: Проектирование службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404297"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="e6293-103">Проектирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e6293-103">Designing a message service</span></span>

<span data-ttu-id="e6293-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6293-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6293-105">Прежде чем приступить к написанию кода для поддержки службы сообщений, важно создать дизайн.</span><span class="sxs-lookup"><span data-stu-id="e6293-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="e6293-106">Устранение следующих проблем в процессе разработки:</span><span class="sxs-lookup"><span data-stu-id="e6293-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="e6293-107">Определите, сколько поставщиков услуг должно быть включено в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="e6293-108">Включите в службу только связанных поставщиков услуг (то есть поставщиков, которые работают с одной и той же системой обмена сообщениями).</span><span class="sxs-lookup"><span data-stu-id="e6293-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="e6293-109">Несвязанные поставщики услуг не принадлежат к одной и той же службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="e6293-110">Используйте профиль для интеграции несвязанных поставщиков услуг и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="e6293-111">Определите, какой тип поставщиков услуг должен быть включен в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="e6293-112">Большинство служб messge включают по одному поставщику каждого из общих типов.</span><span class="sxs-lookup"><span data-stu-id="e6293-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="e6293-113">То есть у обычной службы сообщений есть один поставщик адресной книги, один поставщик магазинов сообщений и один поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="e6293-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="e6293-114">Определите, сколько DLLs должно содержать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="e6293-115">Количество DLLs, которое использует служба сообщений, зависит от следующих:</span><span class="sxs-lookup"><span data-stu-id="e6293-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="e6293-116">Степень сложности, которую вы, как автор службы сообщений, готовы обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="e6293-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="e6293-117">Тип поставщиков услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="e6293-118">Связь службы сообщений с другой службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="e6293-119">Так как MAPI хранит только одну точку входа для каждого типа поставщика, не включай несколько поставщиков одного типа в один DLL.</span><span class="sxs-lookup"><span data-stu-id="e6293-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="e6293-120">Если имеет смысл включать несколько поставщиков одного типа, либо реализуйте их в отдельные DLLs, либо ведите их совместно с функцией точки входа.</span><span class="sxs-lookup"><span data-stu-id="e6293-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="e6293-121">Другой вариант — реализовать связанные службы сообщений или службы сообщений, которые могут использовать один и тот же код установки и конфигурации и ту же функцию точек входа DLL в одной DLL.</span><span class="sxs-lookup"><span data-stu-id="e6293-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="e6293-122">По возможности сохраняйте его простым и используйте один DLL, содержащий реализацию всех поставщиков услуг в службе сообщений и весь код для установки и настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6293-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="e6293-123">Если это невозможно, можно реализовать один DLL для кода установки и конфигурации, а также один DLL для всех поставщиков услуг или один DLL для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6293-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="e6293-124">Определите имя службы сообщений DLL или DLLs.</span><span class="sxs-lookup"><span data-stu-id="e6293-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e6293-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e6293-125">See also</span></span>

- [<span data-ttu-id="e6293-126">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e6293-126">Message Service Implementation</span></span>](message-service-implementation.md)

