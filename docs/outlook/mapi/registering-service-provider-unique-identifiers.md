---
title: Регистрация уникальных идентификаторов поставщиков служб
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bde7ff73f58c8809d2dd6467daea28461e7c6ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586272"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="3c2ce-103">Регистрация уникальных идентификаторов поставщиков служб</span><span class="sxs-lookup"><span data-stu-id="3c2ce-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="3c2ce-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c2ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c2ce-105">Адресной книги, хранилища сообщений и поставщиками транспорта использование уникального идентификатора, называемого [MAPIUID](mapiuid.md) для регистрации в службе объекты различных типов.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="3c2ce-106">**MAPIUID** является идентификатором 16-битное, содержащая GUID.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="3c2ce-107">**MAPIUID** можно создать с помощью следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="3c2ce-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="3c2ce-108">Определите константу.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-108">Define a constant.</span></span>
    
2. <span data-ttu-id="3c2ce-109">Вызов Visual Studio*Создать GUID*\* средство.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="3c2ce-110">Например поставщика адресных книг может включать следующие константы в файл заголовка для определения **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="3c2ce-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="3c2ce-111">**Чтобы зарегистрировать MAPIUID, если ваш поставщик является поставщик адресной книги или сообщения хранилища**</span><span class="sxs-lookup"><span data-stu-id="3c2ce-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="3c2ce-112">Вызов [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ce-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="3c2ce-113">Регистрация **MAPIUID** для каждого входа создания экземпляра и включить в этом **MAPIUID** в первых 16 байтов **ab** членом каждый идентификатор записи, создаваемого объектов.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="3c2ce-114">MAPI использует **MAPIUID** структуры для связи с поставщиками услуг объекты.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="3c2ce-115">Если клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) , чтобы открыть объект MAPI проверяет **MAPIUID** часть идентификатор записи, сравнение с зарегистрированным **MAPIUID**, чтобы определить, какой объект входа в систему следует направить open запрос.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="3c2ce-116">Если ваш поставщик транспорта, зарегистрируйте структуры один или несколько **MAPIUID** при MAPI вызывает метод **IXPLogon::AddressTypes** .</span><span class="sxs-lookup"><span data-stu-id="3c2ce-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="3c2ce-117">MAPI использует **MAPIUID** структуры, зарегистрированные поставщиками транспорта для назначения ответственности для доставки сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="3c2ce-118">Хотя для поставщиков услуг обычно зарегистрировать одного **MAPIUID**, можно регистрировать несколько структур **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="3c2ce-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="3c2ce-119">Если адресной книги или сообщения хранить поставщик поддерживает несколько объектов входа в систему, возможно, позволяя пользователям добавлять несколько экземпляров поставщика для своего профиля, можно реализовать различные **MAPIUID** для каждого объекта входа в систему.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="3c2ce-120">Существует несколько других причин для поддержки нескольких **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="3c2ce-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="3c2ce-121">Должен поддерживать несколько версий поставщика и идентификаторы записей должен представлять соответствующую версию.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="3c2ce-122">Назначьте разные **MAPIUID** для каждой из версий.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="3c2ce-123">Вы хотите различать типы объектов, которые вы поддерживаете.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="3c2ce-124">Например поставщика адресных книг может потребоваться регистрации одной **MAPIUID** для использования в идентификаторах запись обмена сообщениями объектов пользователей и различных **MAPIUID** для списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="3c2ce-125">При наличии нескольких объектов входа в систему, одновременно активны, имеет смысл иметь уникальные **MAPIUID** структуры для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="3c2ce-126">Это повышает точность, с которым MAPI сопоставляет идентификаторы записей для поставщиков услуг и сохраняет определенные операции.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="3c2ce-127">Когда каждый объект входа имеет свой собственный уникальный идентификатор, MAPI можно гарантирует, что любые запросить маршрутов объект входа могут быть обработаны этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="3c2ce-128">После входа в систему объекты совместно используют **MAPIUID** структуры, MAPI направляет запрос первый объект входа в систему, который идентифицируется средством **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="3c2ce-129">Если один из объектов входа получает запрос, который он не может обработать, так как он не обрабатывает идентификатор записи, передайте запрос к следующему объекту входа в систему перед сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3c2ce-130">См. также</span><span class="sxs-lookup"><span data-stu-id="3c2ce-130">See also</span></span>



[<span data-ttu-id="3c2ce-131">Реализация входа для поставщика службы</span><span class="sxs-lookup"><span data-stu-id="3c2ce-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

