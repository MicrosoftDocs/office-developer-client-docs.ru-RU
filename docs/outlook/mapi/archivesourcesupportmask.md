---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418094"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="dc3f0-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="dc3f0-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="dc3f0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc3f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc3f0-105">Указывает, следует ли Microsoft Office Outlook сканировать папки в хранилище и архивировать их автоматически.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc3f0-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="dc3f0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc3f0-107">В:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="dc3f0-108">[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="dc3f0-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="dc3f0-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-109">Created by:</span></span>  <br/> |<span data-ttu-id="dc3f0-110">Поставщик магазина</span><span class="sxs-lookup"><span data-stu-id="dc3f0-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="dc3f0-111">Доступ к нему можно получить с помощью:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="dc3f0-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="dc3f0-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="dc3f0-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-113">Property type:</span></span>  <br/> |<span data-ttu-id="dc3f0-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc3f0-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc3f0-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-115">Access type:</span></span>  <br/> |<span data-ttu-id="dc3f0-116">Только для чтения или чтения и записи в зависимости от поставщика магазина</span><span class="sxs-lookup"><span data-stu-id="dc3f0-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc3f0-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc3f0-117">Remarks</span></span>

<span data-ttu-id="dc3f0-118">Чтобы предоставить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть действительный тег свойства для любого из этих свойств, переданных в вызов [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="dc3f0-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="dc3f0-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="dc3f0-120">Поставщики магазина могут вызывать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или настроить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="dc3f0-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="dc3f0-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="dc3f0-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc3f0-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="dc3f0-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="dc3f0-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="dc3f0-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-125">ulKind:</span></span>  <br/> |<span data-ttu-id="dc3f0-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="dc3f0-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="dc3f0-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="dc3f0-128">L"ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="dc3f0-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="dc3f0-129">Это свойство позволяет поставщикам хранилищ указывать, следует ли Outlook проверять папки в хранилище и архивировать их автоматически.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="dc3f0-130">По умолчанию это свойство не выставит в магазине, что означает, что Outlook может сканировать папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="dc3f0-131">Если свойство имеется, возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="dc3f0-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dc3f0-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="dc3f0-133">Outlook может сканировать папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="dc3f0-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="dc3f0-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="dc3f0-135">Outlook не должен сканировать папки в магазине.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="dc3f0-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="dc3f0-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="dc3f0-137">Не разрешайте клиентам изменять это свойство в магазине.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="dc3f0-138">Обратите внимание, что **константа ASM_CLIENT_DO_NOT_CHANGE** для дальнейшего справочника и в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="dc3f0-139">На данный момент магазин может запретить клиентам изменять этот флаг, жестко задав значение, возвращаемую магазином для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

