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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281594"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="12944-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="12944-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="12944-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12944-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12944-105">Указывает, следует ли Microsoft Office Outlook сканировать папки в хранилище и автоматически архивировать их.</span><span class="sxs-lookup"><span data-stu-id="12944-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="12944-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="12944-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12944-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="12944-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="12944-108">[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="12944-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="12944-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="12944-109">Created by:</span></span>  <br/> |<span data-ttu-id="12944-110">Поставщик хранилища</span><span class="sxs-lookup"><span data-stu-id="12944-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="12944-111">Доступ:</span><span class="sxs-lookup"><span data-stu-id="12944-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="12944-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="12944-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="12944-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="12944-113">Property type:</span></span>  <br/> |<span data-ttu-id="12944-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="12944-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="12944-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="12944-115">Access type:</span></span>  <br/> |<span data-ttu-id="12944-116">Только чтение или чтение и запись в зависимости от поставщика услуг хранения</span><span class="sxs-lookup"><span data-stu-id="12944-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12944-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="12944-117">Remarks</span></span>

<span data-ttu-id="12944-118">Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMAPIProp: IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданного в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="12944-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="12944-119">Когда тег свойства для любого из этих свойств передается в [IMAPIProp::](imapiprop-getprops.md)-Props, поставщик хранилища также должен возвращать правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="12944-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="12944-120">Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств.</span><span class="sxs-lookup"><span data-stu-id="12944-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="12944-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="12944-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="12944-122">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="12944-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12944-123">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="12944-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="12944-124">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="12944-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="12944-125">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="12944-125">ulKind:</span></span>  <br/> |<span data-ttu-id="12944-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="12944-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="12944-127">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="12944-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="12944-128">L "Арчивесаурцесуппортмаск"</span><span class="sxs-lookup"><span data-stu-id="12944-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="12944-129">Это свойство позволяет поставщикам магазина указать, следует ли Outlook проверять папки в хранилище и автоматически архивировать их.</span><span class="sxs-lookup"><span data-stu-id="12944-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="12944-130">По умолчанию это свойство не отображается в хранилище, что означает, что Outlook может сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="12944-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="12944-131">Если свойство предоставлено, могут быть доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="12944-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="12944-132">АСМ_ДЕФАУЛТ</span><span class="sxs-lookup"><span data-stu-id="12944-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="12944-133">Outlook может сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="12944-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="12944-134">АСМ_ДО_НОТ_АРЧИВЕ</span><span class="sxs-lookup"><span data-stu-id="12944-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="12944-135">Outlook не должен сканировать папки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="12944-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="12944-136">АСМ_КЛИЕНТ_ДО_НОТ_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="12944-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="12944-137">Не разрешать клиентам изменять это свойство в хранилище.</span><span class="sxs-lookup"><span data-stu-id="12944-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="12944-138">Обратите внимание, что константа **асм_клиент_до_нот_чанже** предназначена для использования в будущем и в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="12944-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="12944-139">Пока хранилище может запретить клиентам изменять этот флаг, хардкодинг значение, которое возвращает магазин для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="12944-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

