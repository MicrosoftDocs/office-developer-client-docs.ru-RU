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
ms.openlocfilehash: a1754a7c82d7164617c97df97b762efb1555ccda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808227"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="8942b-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="8942b-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="8942b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8942b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8942b-105">Указывает, будет ли Microsoft Office Outlook необходимо сканировать папки хранилища, включая папки контактов, календаря и задач, при загрузке системы для заполнения области навигации.</span><span class="sxs-lookup"><span data-stu-id="8942b-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8942b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8942b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8942b-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="8942b-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="8942b-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="8942b-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="8942b-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="8942b-109">Created by:</span></span>  <br/> |<span data-ttu-id="8942b-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="8942b-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="8942b-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="8942b-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="8942b-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="8942b-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="8942b-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="8942b-113">Property type:</span></span>  <br/> |<span data-ttu-id="8942b-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8942b-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8942b-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="8942b-115">Access type:</span></span>  <br/> |<span data-ttu-id="8942b-116">Только чтение или чтение и запись в зависимости от поставщика хранилища</span><span class="sxs-lookup"><span data-stu-id="8942b-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8942b-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="8942b-117">Remarks</span></span>

<span data-ttu-id="8942b-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="8942b-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="8942b-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="8942b-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="8942b-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="8942b-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="8942b-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="8942b-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="8942b-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="8942b-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8942b-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="8942b-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="8942b-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8942b-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8942b-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="8942b-125">ulKind:</span></span>  <br/> |<span data-ttu-id="8942b-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="8942b-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="8942b-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="8942b-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="8942b-128">L «CrawlSourceSupportMask»</span><span class="sxs-lookup"><span data-stu-id="8942b-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="8942b-129">Это свойство позволяет поставщиков хранилища указать, должна ли Outlook сканировать различных папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8942b-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="8942b-130">Используется при запуске Outlook проверок существующие папки для каждого открытого хранилища для заполнения области **переходов** ; Outlook проверяет наличие и значение этого свойства для хранилища перед началом сканирования.</span><span class="sxs-lookup"><span data-stu-id="8942b-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="8942b-131">По умолчанию это свойство не доступен для хранилища, это значит, что Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8942b-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="8942b-132">Если свойство предоставляется, ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="8942b-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="8942b-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="8942b-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="8942b-134">Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8942b-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="8942b-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="8942b-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="8942b-136">Outlook не следует сканировать папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8942b-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="8942b-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8942b-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="8942b-138">Не разрешать клиентов для изменения этого свойства в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8942b-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="8942b-139">Обратите внимание на то, что константу **CSM_CLIENT_DO_NOT_CHANGE** является для последующего использования и не реализованы в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8942b-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="8942b-140">Теперь хранилище можно запретить изменять этот флаг, жестко значение, которое возвращает хранилище для этого свойства клиентов.</span><span class="sxs-lookup"><span data-stu-id="8942b-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

