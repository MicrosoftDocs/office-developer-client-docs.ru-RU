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
# <a name="make-store-type-private-property"></a><span data-ttu-id="ad853-103">Make Store Type Private Property</span><span class="sxs-lookup"><span data-stu-id="ad853-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="ad853-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad853-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad853-105">Относится к вторичному магазину как к частному.</span><span class="sxs-lookup"><span data-stu-id="ad853-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ad853-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ad853-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad853-107">Выставлено на:</span><span class="sxs-lookup"><span data-stu-id="ad853-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="ad853-108">[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="ad853-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="ad853-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="ad853-109">Created by:</span></span>  <br/> |<span data-ttu-id="ad853-110">Поставщик магазинов</span><span class="sxs-lookup"><span data-stu-id="ad853-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="ad853-111">Доступ к ним:</span><span class="sxs-lookup"><span data-stu-id="ad853-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="ad853-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="ad853-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="ad853-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="ad853-113">Property type:</span></span>  <br/> |<span data-ttu-id="ad853-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ad853-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ad853-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="ad853-115">Access type:</span></span>  <br/> |<span data-ttu-id="ad853-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad853-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad853-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad853-117">Remarks</span></span>

<span data-ttu-id="ad853-118">Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) и вернуть допустимый тег свойства для любого из этих свойств, переданный [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="ad853-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="ad853-119">Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="ad853-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="ad853-120">Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ad853-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="ad853-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="ad853-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="ad853-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="ad853-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad853-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="ad853-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="ad853-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ad853-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="ad853-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="ad853-125">ulKind:</span></span>  <br/> |<span data-ttu-id="ad853-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="ad853-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="ad853-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="ad853-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="ad853-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="ad853-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="ad853-129">Поставщик магазина может использовать это свойство, чтобы Outlook рассматривать его как частное, если оно является вторичным хранилищем для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad853-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="ad853-130">По умолчанию Outlook для вторичного магазина так же, как и для магазина делегирования, а элементы в вторичном магазине являются закрытыми, только если пользователь пометит их как частные.</span><span class="sxs-lookup"><span data-stu-id="ad853-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="ad853-131">Если это свойство **верно,** элементы, удаленные из вторичного магазина, перемещаются в папку **"Удаленные** элементы" в основном магазине.</span><span class="sxs-lookup"><span data-stu-id="ad853-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="ad853-132">Элементы, отмеченные закрытыми, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="ad853-132">Items marked private are not displayed.</span></span> <span data-ttu-id="ad853-133">Черновики хранятся в папке Черновики в основном хранилище.</span><span class="sxs-lookup"><span data-stu-id="ad853-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="ad853-134">Это свойство игнорируется, если версия Outlook более ранней Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение является **ложным.**</span><span class="sxs-lookup"><span data-stu-id="ad853-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

