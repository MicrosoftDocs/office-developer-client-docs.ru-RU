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
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811617"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="3b190-103">Каноническое свойство PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="3b190-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="3b190-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b190-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b190-105">Содержит имя таблицы (PST-файл) персонального хранилища, который пользователь может изменять, для диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3b190-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b190-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3b190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b190-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="3b190-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="3b190-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3b190-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b190-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="3b190-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="3b190-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3b190-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b190-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b190-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3b190-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3b190-112">Area:</span></span>  <br/> |<span data-ttu-id="3b190-113">Таблица личных папок (.pst) внутренний</span><span class="sxs-lookup"><span data-stu-id="3b190-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b190-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b190-114">Remarks</span></span>

<span data-ttu-id="3b190-115">Если вместо этого используется свойство **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)), откроется диалоговое окно конфигурации, но пользователь не разрешается изменять путь и многие другие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b190-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b190-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b190-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b190-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3b190-117">Protocol specifications</span></span>

<span data-ttu-id="3b190-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3b190-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3b190-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b190-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b190-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3b190-120">Header files</span></span>

<span data-ttu-id="3b190-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b190-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b190-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3b190-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b190-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b190-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3b190-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="3b190-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b190-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3b190-125">See also</span></span>



[<span data-ttu-id="3b190-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b190-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b190-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b190-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b190-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3b190-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b190-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3b190-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

