---
title: Каноническое свойство PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341155"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="4dbce-103">Каноническое свойство PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="4dbce-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="4dbce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dbce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dbce-105">Содержит флаг, описывающий состояние хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4dbce-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4dbce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4dbce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dbce-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="4dbce-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="4dbce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4dbce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4dbce-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="4dbce-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="4dbce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4dbce-110">Data type:</span></span>  <br/> |<span data-ttu-id="4dbce-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4dbce-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4dbce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4dbce-112">Area:</span></span>  <br/> |<span data-ttu-id="4dbce-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbce-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dbce-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4dbce-114">Remarks</span></span>

<span data-ttu-id="4dbce-115">Это свойство является динамическим и может изменяться в зависимости от действий пользователя, в отличие от свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4dbce-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="4dbce-116">Можно задать следующее значение:</span><span class="sxs-lookup"><span data-stu-id="4dbce-116">The following value can be set:</span></span>
  
<span data-ttu-id="4dbce-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="4dbce-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="4dbce-118">Пользователь создал один или несколько активных поисков в магазине.</span><span class="sxs-lookup"><span data-stu-id="4dbce-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4dbce-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4dbce-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4dbce-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4dbce-120">Protocol specifications</span></span>

<span data-ttu-id="4dbce-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dbce-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dbce-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4dbce-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4dbce-123">[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dbce-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dbce-124">Указывает допустимые операции для основных объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4dbce-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4dbce-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4dbce-125">Header files</span></span>

<span data-ttu-id="4dbce-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4dbce-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dbce-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4dbce-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4dbce-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4dbce-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4dbce-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4dbce-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dbce-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4dbce-130">See also</span></span>



[<span data-ttu-id="4dbce-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbce-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dbce-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbce-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dbce-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4dbce-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dbce-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4dbce-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

