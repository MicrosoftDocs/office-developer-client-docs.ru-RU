---
title: Make Store Type Private Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428545"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="c1b2b-103">Make Store Type Private Property</span><span class="sxs-lookup"><span data-stu-id="c1b2b-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="c1b2b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1b2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1b2b-105">Обрабатывает вторичное хранилище как частное.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c1b2b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c1b2b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1b2b-107">В:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="c1b2b-108">[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c1b2b-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="c1b2b-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-109">Created by:</span></span>  <br/> |<span data-ttu-id="c1b2b-110">Поставщик магазина</span><span class="sxs-lookup"><span data-stu-id="c1b2b-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="c1b2b-111">Доступ к нему можно получить с помощью:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="c1b2b-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="c1b2b-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="c1b2b-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-113">Property type:</span></span>  <br/> |<span data-ttu-id="c1b2b-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c1b2b-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c1b2b-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-115">Access type:</span></span>  <br/> |<span data-ttu-id="c1b2b-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c1b2b-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b2b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1b2b-117">Remarks</span></span>

<span data-ttu-id="c1b2b-118">Чтобы предоставить любую функциональность магазина, поставщик магазина должен реализовать [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) и вернуть действительный тег свойства для любого из этих свойств, переданных в вызов [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="c1b2b-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="c1b2b-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="c1b2b-120">Поставщики магазина могут вызывать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или настроить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="c1b2b-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c1b2b-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="c1b2b-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b2b-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="c1b2b-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="c1b2b-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="c1b2b-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-125">ulKind:</span></span>  <br/> |<span data-ttu-id="c1b2b-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="c1b2b-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="c1b2b-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="c1b2b-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="c1b2b-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="c1b2b-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="c1b2b-129">Поставщик магазина может использовать это свойство, чтобы Outlook обрабатывал его как личное, когда это дополнительное хранилище для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="c1b2b-130">По умолчанию Outlook обрабатывает дополнительное хранилище так же, как хранилище делегатов, а элементы в дополнительном хранилище являются частными, только если пользователь пометит их как частные.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="c1b2b-131">Если это свойство имеет **значение true,** элементы, удаленные из дополнительного магазина, перемещаются в папку **"Удаленные"** в основном хранилище.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="c1b2b-132">Элементы, помеченные как частные, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-132">Items marked private are not displayed.</span></span> <span data-ttu-id="c1b2b-133">Черновики хранятся в папке "Черновики" в основном хранилище.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="c1b2b-134">Это свойство игнорируется, если версия Outlook является более ранней, чем Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c1b2b-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

