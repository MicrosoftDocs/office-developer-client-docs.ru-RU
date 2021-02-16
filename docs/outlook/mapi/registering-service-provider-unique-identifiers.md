---
title: Регистрация уникальных идентификаторов поставщика услуг
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410177"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="82862-103">Регистрация уникальных идентификаторов поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="82862-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="82862-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82862-105">Поставщики адресной книги, хранения сообщений и транспорта используют уникальный идентификатор [MAPIUID](mapiuid.md) для регистрации в объектах-службах различных типов.</span><span class="sxs-lookup"><span data-stu-id="82862-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="82862-106">**MAPIUID** — это 16-byte-идентификатор, содержащий GUID.</span><span class="sxs-lookup"><span data-stu-id="82862-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="82862-107">**MapIUID можно** создать с помощью следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="82862-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="82862-108">Определите константы.</span><span class="sxs-lookup"><span data-stu-id="82862-108">Define a constant.</span></span>
    
2. <span data-ttu-id="82862-109">Вызов средства Visual Studio \*GUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="82862-109">Invoke the Visual Studio *Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="82862-110">Например, поставщик адресной книги может включать следующую константу в файле заголовок для определения **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="82862-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="82862-111">**Регистрация MAPIUID, если ваш поставщик является адресной книгой или поставщиком магазина сообщений**</span><span class="sxs-lookup"><span data-stu-id="82862-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="82862-112">Вызов [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="82862-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="82862-113">Зарегистрируйте **MAPIUID** для каждого создаемого объекта входа и включите **этот MAPIUID** в первые 16 bytes **ab-члена** каждого создадаемого идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="82862-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="82862-114">MAPI использует **структуры MAPIUID** для связи объектов с поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="82862-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="82862-115">Когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия объекта, MAPI проверяет часть **MAPIUID** идентификатора записи, соотнося ее с зарегистрированным **MAPIUID,** чтобы определить, какой объект входа должен получить открытый запрос.</span><span class="sxs-lookup"><span data-stu-id="82862-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="82862-116">Если ваш поставщик является транспортом, зарегистрируйте одну или несколько структур **MAPIUID,** когда MAPI вызывает метод **IXPLogon::AddressTypes.**</span><span class="sxs-lookup"><span data-stu-id="82862-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="82862-117">MAPI использует структуры **MAPIUID,** зарегистрированные поставщиками транспорта, для назначения ответственности за доставку сообщений.</span><span class="sxs-lookup"><span data-stu-id="82862-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="82862-118">Хотя поставщики услуг обычно регистрируют один **MAPIUID,** можно зарегистрировать несколько **структур MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="82862-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="82862-119">Если ваша адресная книга или поставщик службы хранения сообщений поддерживает несколько объектов для логотипа, например, разрешив пользователю добавлять в свой профиль несколько экземпляров поставщика, может потребоваться реализовать разные **mapIUID** для каждого объекта для логотипа.</span><span class="sxs-lookup"><span data-stu-id="82862-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="82862-120">Существует несколько других причин для поддержки нескольких **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="82862-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="82862-121">Необходимо поддерживать несколько версий поставщика, а идентификаторы записей должны представлять соответствующую версию.</span><span class="sxs-lookup"><span data-stu-id="82862-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="82862-122">Назначьте **разные MAPIUID** для каждой версии.</span><span class="sxs-lookup"><span data-stu-id="82862-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="82862-123">Необходимо различать типы поддерживаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="82862-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="82862-124">Например, поставщику адресной книги может потребоваться зарегистрировать **один MAPIUID** для использования в идентификаторах записей объектов пользователей обмена сообщениями, а другой **MAPIUID** — для списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="82862-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="82862-125">Если одновременно активно несколько объектов для логотипа, имеет смысл использовать уникальные структуры **MAPIUID** для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="82862-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="82862-126">Это повышает точность, с которой MAPI соответствует идентификаторам записей поставщикам услуг и экономит часть работы.</span><span class="sxs-lookup"><span data-stu-id="82862-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="82862-127">Если у каждого объекта для логотипа есть свой уникальный идентификатор, MAPI может гарантировать, что любой запрос, который он перенаправляет в объект для логотипа, может обрабатываться этим объектом.</span><span class="sxs-lookup"><span data-stu-id="82862-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="82862-128">Когда объекты для логотипа имеют обную структуру **MAPIUID,** MAPI маршрутит запрос на первый объект для логотипа, который определен **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="82862-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="82862-129">Если один из объектов входа получает запрос, который не может обработать, так как он не обрабатывает идентификатор записи, перед возвратом ошибки передайте его следующему объекту входа.</span><span class="sxs-lookup"><span data-stu-id="82862-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82862-130">См. также</span><span class="sxs-lookup"><span data-stu-id="82862-130">See also</span></span>



[<span data-ttu-id="82862-131">Реализация службы для логоса</span><span class="sxs-lookup"><span data-stu-id="82862-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

