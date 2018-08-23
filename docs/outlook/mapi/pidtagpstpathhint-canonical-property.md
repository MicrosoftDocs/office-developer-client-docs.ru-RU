---
title: Каноническое свойство PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569094"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="6d823-103">Каноническое свойство PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="6d823-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="6d823-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d823-105">Содержит имя таблицы (PST-файл) персонального хранилища, который пользователь может изменять, для диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6d823-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d823-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d823-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d823-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="6d823-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="6d823-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d823-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d823-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="6d823-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="6d823-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d823-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d823-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d823-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6d823-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d823-112">Area:</span></span>  <br/> |<span data-ttu-id="6d823-113">Таблица личных папок (.pst) внутренний</span><span class="sxs-lookup"><span data-stu-id="6d823-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d823-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d823-114">Remarks</span></span>

<span data-ttu-id="6d823-115">Если вместо этого используется свойство **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)), откроется диалоговое окно конфигурации, но пользователь не разрешается изменять путь и многие другие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d823-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d823-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d823-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d823-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6d823-117">Protocol specifications</span></span>

<span data-ttu-id="6d823-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="6d823-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="6d823-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6d823-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d823-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6d823-120">Header files</span></span>

<span data-ttu-id="6d823-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d823-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d823-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d823-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d823-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d823-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6d823-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6d823-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d823-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6d823-125">See also</span></span>



[<span data-ttu-id="6d823-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d823-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d823-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d823-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d823-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d823-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d823-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d823-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

