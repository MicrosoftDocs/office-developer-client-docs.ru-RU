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
# <a name="designing-a-message-service"></a><span data-ttu-id="dfcb8-103">Проектирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="dfcb8-103">Designing a message service</span></span>

<span data-ttu-id="dfcb8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfcb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfcb8-105">Прежде чем приступить к написанию кода для поддержки службы сообщений, важно создать проект.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="dfcb8-106">Устраните следующие проблемы в процессе создания проекта.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="dfcb8-107">Определите, сколько поставщиков служб должно быть включено в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="dfcb8-108">Включайте в службу только связанные поставщики услуг (то есть поставщики, которые работают с одной и той же системой обмена сообщениями).</span><span class="sxs-lookup"><span data-stu-id="dfcb8-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="dfcb8-109">Несвязанные поставщики услуг не входят в одну и ту же службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="dfcb8-110">Используйте профиль для интеграции несвязанных поставщиков услуг и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="dfcb8-111">Определите, какие типы поставщиков услуг следует включить в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="dfcb8-112">Большинство служб мессже включают один поставщик каждого из общих типов.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="dfcb8-113">То есть обычная служба сообщений имеет одного поставщика адресных книг, одного поставщика хранилища сообщений и одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="dfcb8-114">Определите, сколько библиотек DLL должно содержать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="dfcb8-115">Количество библиотек DLL, которые использует служба сообщений, зависит от следующих условий:</span><span class="sxs-lookup"><span data-stu-id="dfcb8-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="dfcb8-116">Степень сложности, которую вы в качестве автора службы сообщений обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="dfcb8-117">Тип поставщиков услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="dfcb8-118">Связь, которую может иметь служба сообщений, с другой службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="dfcb8-119">Так как MAPI хранит только одну точку входа для каждого типа поставщика, не включайте нескольких поставщиков одного типа в одну БИБЛИОТЕКУ DLL.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="dfcb8-120">Если имеет смысл включить нескольких поставщиков одного типа, их следует реализовать в отдельных библиотеках DLL или предоставить им общий доступ к функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="dfcb8-121">Кроме того, можно реализовать связанные службы сообщений или службы сообщений, которые могут использовать один и тот же код установки и конфигурации и одну и ту же функцию точки входа DLL, в одной DLL.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="dfcb8-122">Если это возможно, храните его простой и используйте одну БИБЛИОТЕКУ DLL, которая содержит реализацию всех поставщиков служб в службе сообщений и весь код для установки и настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="dfcb8-123">Если это невозможно, можно внедрить одну БИБЛИОТЕКУ DLL для кода установки и конфигурации, а также одну БИБЛИОТЕКУ DLL для всех поставщиков услуг или одной библиотеки DLL для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="dfcb8-124">Определите имя библиотеки DLL службы сообщений или библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dfcb8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="dfcb8-125">See also</span></span>

- [<span data-ttu-id="dfcb8-126">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="dfcb8-126">Message Service Implementation</span></span>](message-service-implementation.md)

