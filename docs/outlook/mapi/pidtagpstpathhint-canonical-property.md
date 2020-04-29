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
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437310"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="ced19-103">Каноническое свойство PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="ced19-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="ced19-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced19-105">Предоставляет имя личной таблицы хранения (PST-файла), которую пользователь может редактировать, в диалоговом окне Конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ced19-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ced19-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ced19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ced19-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="ced19-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="ced19-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ced19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ced19-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="ced19-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="ced19-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ced19-110">Data type:</span></span>  <br/> |<span data-ttu-id="ced19-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ced19-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ced19-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ced19-112">Area:</span></span>  <br/> |<span data-ttu-id="ced19-113">Внутренняя таблица хранения личных данных (PST)</span><span class="sxs-lookup"><span data-stu-id="ced19-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ced19-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ced19-114">Remarks</span></span>

<span data-ttu-id="ced19-115">Если вместо этого используется свойство **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)), откроется диалоговое окно Configuration (конфигурация), но пользователю не будет разрешено изменять путь и многие другие свойства.</span><span class="sxs-lookup"><span data-stu-id="ced19-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ced19-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ced19-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ced19-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ced19-117">Protocol specifications</span></span>

<span data-ttu-id="ced19-118">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="ced19-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="ced19-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ced19-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ced19-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ced19-120">Header files</span></span>

<span data-ttu-id="ced19-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ced19-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ced19-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ced19-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ced19-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ced19-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ced19-124">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="ced19-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ced19-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ced19-125">See also</span></span>



[<span data-ttu-id="ced19-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ced19-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ced19-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ced19-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ced19-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ced19-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ced19-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ced19-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

