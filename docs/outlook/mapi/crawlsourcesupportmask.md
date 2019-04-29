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
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="14730-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="14730-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="14730-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14730-105">Указывает, следует ли Microsoft Office Outlook сканировать папки в хранилище, включая папки Контакты, календарь и задачи, при запуске, чтобы заполнить область навигации.</span><span class="sxs-lookup"><span data-stu-id="14730-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="14730-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="14730-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14730-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="14730-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="14730-108">[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="14730-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="14730-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="14730-109">Created by:</span></span>  <br/> |<span data-ttu-id="14730-110">Поставщик хранилища</span><span class="sxs-lookup"><span data-stu-id="14730-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="14730-111">Доступ:</span><span class="sxs-lookup"><span data-stu-id="14730-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="14730-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="14730-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="14730-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="14730-113">Property type:</span></span>  <br/> |<span data-ttu-id="14730-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="14730-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="14730-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="14730-115">Access type:</span></span>  <br/> |<span data-ttu-id="14730-116">Только чтение или чтение и запись в зависимости от поставщика услуг хранения</span><span class="sxs-lookup"><span data-stu-id="14730-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14730-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="14730-117">Remarks</span></span>

<span data-ttu-id="14730-118">Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMAPIProp: IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданного в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="14730-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="14730-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::](imapiprop-getprops.md)-Props, поставщик хранилища также должен возвращать правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="14730-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="14730-120">Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств.</span><span class="sxs-lookup"><span data-stu-id="14730-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="14730-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="14730-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="14730-122">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="14730-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14730-123">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="14730-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="14730-124">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="14730-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="14730-125">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="14730-125">ulKind:</span></span>  <br/> |<span data-ttu-id="14730-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="14730-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="14730-127">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="14730-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="14730-128">L "Кравлсаурцесуппортмаск"</span><span class="sxs-lookup"><span data-stu-id="14730-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="14730-129">Это свойство позволяет поставщикам услуг магазина указывать, следует ли Outlook сканировать различные папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="14730-130">Он используется при запуске, когда Outlook сканирует существующие папки в каждом открытом хранилище для заполнения области **навигации** ; Перед началом сканирования Outlook проверяет наличие и значение этого свойства в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="14730-131">По умолчанию это свойство не отображается в хранилище, что означает, что Outlook может сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="14730-132">Если свойство предоставлено, могут быть доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="14730-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="14730-133">КСМ_ДЕФАУЛТ</span><span class="sxs-lookup"><span data-stu-id="14730-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="14730-134">Outlook может сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="14730-135">КСМ_ДО_НОТ_КРАВЛ</span><span class="sxs-lookup"><span data-stu-id="14730-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="14730-136">Outlook не должен сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="14730-137">КСМ_КЛИЕНТ_ДО_НОТ_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="14730-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="14730-138">Не разрешать клиентам изменять это свойство в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14730-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="14730-139">Обратите внимание, что константа **ксм_клиент_до_нот_чанже** предназначена для использования в будущем и в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="14730-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="14730-140">Пока хранилище может запретить клиентам изменять этот флаг, хардкодинг значение, которое возвращает магазин для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="14730-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

