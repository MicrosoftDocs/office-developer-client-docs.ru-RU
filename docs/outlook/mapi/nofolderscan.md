---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436813"
---
# <a name="nofolderscan"></a><span data-ttu-id="e01a9-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="e01a9-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="e01a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e01a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e01a9-105">Указывает, следует ли Microsoft Office Outlook сканировать папки Contacts в магазине.</span><span class="sxs-lookup"><span data-stu-id="e01a9-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e01a9-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e01a9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e01a9-107">Выставлено на:</span><span class="sxs-lookup"><span data-stu-id="e01a9-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="e01a9-108">[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e01a9-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="e01a9-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="e01a9-109">Created by:</span></span>  <br/> |<span data-ttu-id="e01a9-110">Поставщик магазинов</span><span class="sxs-lookup"><span data-stu-id="e01a9-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="e01a9-111">Доступ к ним:</span><span class="sxs-lookup"><span data-stu-id="e01a9-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="e01a9-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="e01a9-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="e01a9-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="e01a9-113">Property type:</span></span>  <br/> |<span data-ttu-id="e01a9-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e01a9-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e01a9-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="e01a9-115">Access type:</span></span>  <br/> |<span data-ttu-id="e01a9-116">Только для чтения или чтения/записи в зависимости от поставщика магазина</span><span class="sxs-lookup"><span data-stu-id="e01a9-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e01a9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e01a9-117">Remarks</span></span>

<span data-ttu-id="e01a9-118">Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="e01a9-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="e01a9-119">Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="e01a9-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="e01a9-120">Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="e01a9-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="e01a9-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="e01a9-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="e01a9-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="e01a9-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e01a9-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="e01a9-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="e01a9-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e01a9-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e01a9-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="e01a9-125">ulKind:</span></span>  <br/> |<span data-ttu-id="e01a9-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="e01a9-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="e01a9-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="e01a9-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="e01a9-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="e01a9-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="e01a9-129">Это свойство позволяет поставщикам магазинов указать, Outlook не сканировать папки Contacts в магазине, чтобы избежать ухудшения производительности.</span><span class="sxs-lookup"><span data-stu-id="e01a9-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="e01a9-130">Он используется в операциях слияния почты, Outlook проверки на наличие и значение этого свойства перед началом проверки.</span><span class="sxs-lookup"><span data-stu-id="e01a9-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="e01a9-131">По умолчанию это свойство не подвергается воздействию в магазине, что Outlook может сканировать папку Контакты в магазине.</span><span class="sxs-lookup"><span data-stu-id="e01a9-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="e01a9-132">Если свойство выставлено, возможные значения:</span><span class="sxs-lookup"><span data-stu-id="e01a9-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="e01a9-133">Zero (0): Outlook может выполнять сканирование.</span><span class="sxs-lookup"><span data-stu-id="e01a9-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="e01a9-134">Значение Non-zero: Outlook не следует сканировать папки Contacts в магазине.</span><span class="sxs-lookup"><span data-stu-id="e01a9-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

