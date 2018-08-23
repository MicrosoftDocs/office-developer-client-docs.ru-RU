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
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581778"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="5e1d7-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="5e1d7-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="5e1d7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e1d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e1d7-105">Указывает, будет ли Microsoft Office Outlook необходимо сканировать папки хранилища, включая папки контактов, календаря и задач, при загрузке системы для заполнения области навигации.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5e1d7-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5e1d7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e1d7-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="5e1d7-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="5e1d7-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="5e1d7-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-109">Created by:</span></span>  <br/> |<span data-ttu-id="5e1d7-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="5e1d7-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="5e1d7-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="5e1d7-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="5e1d7-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="5e1d7-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-113">Property type:</span></span>  <br/> |<span data-ttu-id="5e1d7-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e1d7-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e1d7-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-115">Access type:</span></span>  <br/> |<span data-ttu-id="5e1d7-116">Только чтение или чтение и запись в зависимости от поставщика хранилища</span><span class="sxs-lookup"><span data-stu-id="5e1d7-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e1d7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="5e1d7-117">Remarks</span></span>

<span data-ttu-id="5e1d7-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="5e1d7-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="5e1d7-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="5e1d7-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="5e1d7-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="5e1d7-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e1d7-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="5e1d7-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5e1d7-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5e1d7-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-125">ulKind:</span></span>  <br/> |<span data-ttu-id="5e1d7-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5e1d7-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="5e1d7-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="5e1d7-128">L «CrawlSourceSupportMask»</span><span class="sxs-lookup"><span data-stu-id="5e1d7-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="5e1d7-129">Это свойство позволяет поставщиков хранилища указать, должна ли Outlook сканировать различных папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="5e1d7-130">Используется при запуске Outlook проверок существующие папки для каждого открытого хранилища для заполнения области **переходов** ; Outlook проверяет наличие и значение этого свойства для хранилища перед началом сканирования.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="5e1d7-131">По умолчанию это свойство не доступен для хранилища, это значит, что Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="5e1d7-132">Если свойство предоставляется, ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="5e1d7-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="5e1d7-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5e1d7-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="5e1d7-134">Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="5e1d7-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="5e1d7-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="5e1d7-136">Outlook не следует сканировать папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="5e1d7-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5e1d7-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="5e1d7-138">Не разрешать клиентов для изменения этого свойства в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="5e1d7-139">Обратите внимание на то, что константу **CSM_CLIENT_DO_NOT_CHANGE** является для последующего использования и не реализованы в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="5e1d7-140">Теперь хранилище можно запретить изменять этот флаг, жестко значение, которое возвращает хранилище для этого свойства клиентов.</span><span class="sxs-lookup"><span data-stu-id="5e1d7-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

