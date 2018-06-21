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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19808064"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="cde47-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="cde47-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="cde47-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cde47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cde47-105">Разрешение следует сканировать папок в хранилище и архивировать их автоматически Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="cde47-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cde47-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="cde47-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cde47-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="cde47-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="cde47-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="cde47-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="cde47-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="cde47-109">Created by:</span></span>  <br/> |<span data-ttu-id="cde47-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="cde47-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="cde47-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="cde47-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="cde47-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="cde47-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="cde47-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="cde47-113">Property type:</span></span>  <br/> |<span data-ttu-id="cde47-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cde47-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cde47-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="cde47-115">Access type:</span></span>  <br/> |<span data-ttu-id="cde47-116">Только чтение или чтение и запись в зависимости от поставщика хранилища</span><span class="sxs-lookup"><span data-stu-id="cde47-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cde47-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="cde47-117">Remarks</span></span>

<span data-ttu-id="cde47-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="cde47-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="cde47-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="cde47-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="cde47-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cde47-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="cde47-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="cde47-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="cde47-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="cde47-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cde47-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="cde47-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="cde47-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cde47-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cde47-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="cde47-125">ulKind:</span></span>  <br/> |<span data-ttu-id="cde47-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="cde47-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="cde47-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="cde47-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="cde47-128">L «ArchiveSourceSupportMask»</span><span class="sxs-lookup"><span data-stu-id="cde47-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="cde47-129">Это свойство позволяет поставщиков хранилища для указания ли Outlook следует сканировать папок в хранилище и архивировать их автоматически.</span><span class="sxs-lookup"><span data-stu-id="cde47-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="cde47-130">По умолчанию это свойство не доступен для хранилища, это значит, что Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cde47-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="cde47-131">Если свойство предоставляется, ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="cde47-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="cde47-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="cde47-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="cde47-133">Outlook поддерживает сканирование папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cde47-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="cde47-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="cde47-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="cde47-135">Outlook не следует сканировать папок в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cde47-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="cde47-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="cde47-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="cde47-137">Не разрешать клиентов для изменения этого свойства в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cde47-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="cde47-138">Обратите внимание на то, что константу **ASM_CLIENT_DO_NOT_CHANGE** является для последующего использования и не реализованы в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="cde47-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="cde47-139">Теперь хранилище можно запретить изменять этот флаг, жестко значение, которое возвращает хранилище для этого свойства клиентов.</span><span class="sxs-lookup"><span data-stu-id="cde47-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

