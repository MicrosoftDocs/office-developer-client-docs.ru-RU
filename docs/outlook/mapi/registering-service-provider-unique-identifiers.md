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
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328401"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="c5aa3-103">Регистрация уникальных идентификаторов поставщиков служб</span><span class="sxs-lookup"><span data-stu-id="c5aa3-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="c5aa3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5aa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5aa3-105">Адресная книга, хранилище сообщений и поставщики транспорта используют уникальный идентификатор, который называется [мапиуид](mapiuid.md) для регистрации в объектах обслуживания различных типов.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="c5aa3-106">**Мапиуид** — это 16-байтовый идентификатор, который содержит GUID.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="c5aa3-107">Вы можете создать **мапиуид** с помощью следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="c5aa3-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="c5aa3-108">Определите константу.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-108">Define a constant.</span></span>
    
2. <span data-ttu-id="c5aa3-109">Запустите средство Visual Studio\*CREATE GUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="c5aa3-110">Например, у поставщика адресных книг может быть следующая константа в файле заголовка для определения объекта **мапиуид**:</span><span class="sxs-lookup"><span data-stu-id="c5aa3-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="c5aa3-111">**Регистрация МАПИУИД, если поставщик является адресной книгой или поставщиком хранилища сообщений**</span><span class="sxs-lookup"><span data-stu-id="c5aa3-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="c5aa3-112">Call [имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="c5aa3-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="c5aa3-113">ЗаРегистрируйте **мапиуид** для каждого объекта входа, который вы создаете, и включите этот **мапиуид** в первые 16 байт элемента **AB** каждого идентификатора записи, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="c5aa3-114">Для связи объектов с поставщиками службы MAPI использует структуры **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="c5aa3-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="c5aa3-115">Когда клиент вызывает метод [IMAPISession:: OpenEntry](imapisession-openentry.md) для открытия объекта, MAPI проверяет часть идентификатора записи **мапиуид** , сопоставляя ее с зарегистрированным **мапиуид**, чтобы определить, какой объект входа должен получать Открытый Request.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="c5aa3-116">Если ваш поставщик является транспортом, зарегистрируйте одну или несколько структур **мапиуид** , когда MAPI вызывает метод **Иксплогон:: аддресстипес** .</span><span class="sxs-lookup"><span data-stu-id="c5aa3-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="c5aa3-117">MAPI использует структуры **мапиуид** , зарегистрированные поставщиками транспорта, для назначения ответственных за доставку сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="c5aa3-118">Хотя поставщики услуг обычно регистрируют один **мапиуид**, вы можете зарегистрировать несколько структур **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="c5aa3-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="c5aa3-119">Если ваша адресная книга или поставщик хранилища сообщений поддерживает несколько объектов входа в систему, возможно, путем добавления нескольких экземпляров поставщика в свой профиль, может потребоваться реализация разных **мапиуид** для каждого объекта logon.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="c5aa3-120">Существует несколько других причин для поддержки более одного **мапиуид**:</span><span class="sxs-lookup"><span data-stu-id="c5aa3-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="c5aa3-121">Необходимо поддерживать более одной версии поставщика, и идентификаторы записей должны представлять соответствующую версию.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="c5aa3-122">Назначьте разные **мапиуид** для каждой версии.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="c5aa3-123">Необходимо различать типы поддерживаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="c5aa3-124">Например, поставщику адресной книги может понадобиться зарегистрировать один **мапиуид** для использования в идентификаторах записей для объектов-пользователей обмена сообщениями и другой **мапиуид** для использования в списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="c5aa3-125">При наличии нескольких одновременно активных объектов входа имеет смысл иметь уникальные структуры **мапиуид** для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="c5aa3-126">Это повышает точность, с которой MAPI сопоставляет идентификаторы записей с поставщиками услуг и сохраняет некоторую работу.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="c5aa3-127">Когда каждый объект logon имеет собственный уникальный идентификатор, MAPI может гарантировать, что любой запрос, переданный в объект logon, может обрабатываться этим объектом.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="c5aa3-128">Когда объекты входа совместно используют структуры **мапиуид** , MAPI направляет запрос в первый объект logon, идентифицированный параметром **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="c5aa3-129">Если один из ваших объектов входа получает запрос, который не может быть обработан, так как он не обрабатывает идентификатор записи, перед возвращением ошибки перед возвращением запроса передается в следующий объект logon.</span><span class="sxs-lookup"><span data-stu-id="c5aa3-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5aa3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c5aa3-130">See also</span></span>



[<span data-ttu-id="c5aa3-131">Реализация входа у поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="c5aa3-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

