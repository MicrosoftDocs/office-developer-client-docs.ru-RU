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
ms.openlocfilehash: 7348d0395952036ee6b356b013072324b64e4b98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570823"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="91d61-103">Каноническое свойство PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="91d61-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="91d61-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91d61-105">Содержит флаг, который описывает состояние хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="91d61-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91d61-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91d61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91d61-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="91d61-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="91d61-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="91d61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91d61-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="91d61-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="91d61-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91d61-110">Data type:</span></span>  <br/> |<span data-ttu-id="91d61-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91d61-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91d61-112">Область:</span><span class="sxs-lookup"><span data-stu-id="91d61-112">Area:</span></span>  <br/> |<span data-ttu-id="91d61-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="91d61-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91d61-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="91d61-114">Remarks</span></span>

<span data-ttu-id="91d61-115">Это свойство является динамическим и может изменяться в зависимости от действий пользователя, в отличие от свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91d61-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="91d61-116">Может быть установлено следующее значение:</span><span class="sxs-lookup"><span data-stu-id="91d61-116">The following value can be set:</span></span>
  
<span data-ttu-id="91d61-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="91d61-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="91d61-118">Пользователь мог создать один или несколько активных поисков в хранилище.</span><span class="sxs-lookup"><span data-stu-id="91d61-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="91d61-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91d61-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91d61-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91d61-120">Protocol specifications</span></span>

<span data-ttu-id="91d61-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d61-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d61-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="91d61-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91d61-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d61-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d61-124">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="91d61-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91d61-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="91d61-125">Header files</span></span>

<span data-ttu-id="91d61-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91d61-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="91d61-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91d61-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="91d61-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91d61-128">Mapitags.h</span></span>
  
> <span data-ttu-id="91d61-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="91d61-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91d61-130">См. также</span><span class="sxs-lookup"><span data-stu-id="91d61-130">See also</span></span>



[<span data-ttu-id="91d61-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91d61-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91d61-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91d61-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91d61-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91d61-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91d61-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="91d61-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

