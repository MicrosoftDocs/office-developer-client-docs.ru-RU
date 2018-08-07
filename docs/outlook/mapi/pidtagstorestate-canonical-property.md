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
ms.openlocfilehash: a50a38825434ef1e76f0ea5ff2e4d6d5d847a975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812008"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="96934-103">Каноническое свойство PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="96934-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="96934-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96934-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96934-105">Содержит флаг, который описывает состояние хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="96934-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96934-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="96934-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96934-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="96934-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="96934-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="96934-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96934-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="96934-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="96934-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="96934-110">Data type:</span></span>  <br/> |<span data-ttu-id="96934-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="96934-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="96934-112">Область:</span><span class="sxs-lookup"><span data-stu-id="96934-112">Area:</span></span>  <br/> |<span data-ttu-id="96934-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="96934-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96934-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="96934-114">Remarks</span></span>

<span data-ttu-id="96934-115">Это свойство является динамическим и может изменяться в зависимости от действий пользователя, в отличие от свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96934-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="96934-116">Может быть установлено следующее значение:</span><span class="sxs-lookup"><span data-stu-id="96934-116">The following value can be set:</span></span>
  
<span data-ttu-id="96934-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="96934-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="96934-118">Пользователь мог создать один или несколько активных поисков в хранилище.</span><span class="sxs-lookup"><span data-stu-id="96934-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="96934-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96934-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96934-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="96934-120">Protocol specifications</span></span>

<span data-ttu-id="96934-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96934-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96934-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96934-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96934-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96934-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96934-124">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="96934-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96934-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="96934-125">Header files</span></span>

<span data-ttu-id="96934-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96934-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="96934-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="96934-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="96934-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96934-128">Mapitags.h</span></span>
  
> <span data-ttu-id="96934-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="96934-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96934-130">См. также</span><span class="sxs-lookup"><span data-stu-id="96934-130">See also</span></span>



[<span data-ttu-id="96934-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96934-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96934-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96934-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96934-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="96934-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96934-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="96934-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

