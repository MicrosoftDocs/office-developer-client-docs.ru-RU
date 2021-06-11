---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420915"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="a1b30-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="a1b30-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="a1b30-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1b30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1b30-105">Указывает, следует ли Microsoft Office Outlook в магазине, включая папки Contacts, Calendar и Tasks, при запуске для заполнения области навигации.</span><span class="sxs-lookup"><span data-stu-id="a1b30-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a1b30-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a1b30-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1b30-107">Выставлено на:</span><span class="sxs-lookup"><span data-stu-id="a1b30-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="a1b30-108">[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a1b30-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="a1b30-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="a1b30-109">Created by:</span></span>  <br/> |<span data-ttu-id="a1b30-110">Поставщик магазинов</span><span class="sxs-lookup"><span data-stu-id="a1b30-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="a1b30-111">Доступ к ним:</span><span class="sxs-lookup"><span data-stu-id="a1b30-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="a1b30-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="a1b30-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="a1b30-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="a1b30-113">Property type:</span></span>  <br/> |<span data-ttu-id="a1b30-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a1b30-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a1b30-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="a1b30-115">Access type:</span></span>  <br/> |<span data-ttu-id="a1b30-116">Только для чтения или чтения/записи в зависимости от поставщика магазина</span><span class="sxs-lookup"><span data-stu-id="a1b30-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1b30-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1b30-117">Remarks</span></span>

<span data-ttu-id="a1b30-118">Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="a1b30-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="a1b30-119">Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a1b30-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="a1b30-120">Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a1b30-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="a1b30-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="a1b30-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="a1b30-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="a1b30-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b30-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="a1b30-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="a1b30-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a1b30-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a1b30-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="a1b30-125">ulKind:</span></span>  <br/> |<span data-ttu-id="a1b30-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="a1b30-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="a1b30-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="a1b30-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="a1b30-128">L"CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="a1b30-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="a1b30-129">Это свойство позволяет поставщикам магазинов указать, следует ли Outlook сканировать различные папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="a1b30-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="a1b30-130">Он используется при запуске, Outlook сканирует существующие папки в каждом открытом магазине для заполнения области **навигации;** Outlook проверить наличие и значение этого свойства в магазине перед началом проверки.</span><span class="sxs-lookup"><span data-stu-id="a1b30-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="a1b30-131">По умолчанию это свойство не подвергается воздействию в магазине, что Outlook может проверять папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="a1b30-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="a1b30-132">Если свойство выставлено, возможные значения:</span><span class="sxs-lookup"><span data-stu-id="a1b30-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="a1b30-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="a1b30-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="a1b30-134">Outlook можно сканировать папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="a1b30-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="a1b30-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="a1b30-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="a1b30-136">Outlook не следует сканировать папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="a1b30-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="a1b30-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a1b30-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="a1b30-138">Не позволяйте клиентам изменять это свойство в магазине.</span><span class="sxs-lookup"><span data-stu-id="a1b30-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="a1b30-139">Обратите внимание, **что CSM_CLIENT_DO_NOT_CHANGE** для будущей ссылки и в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="a1b30-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="a1b30-140">В настоящее время магазин может запретить клиентам изменять этот флаг, жестко задав значение, которое возвращает хранилище для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a1b30-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

