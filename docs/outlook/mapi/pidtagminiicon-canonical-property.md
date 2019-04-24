---
title: Каноническое свойство PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356233"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="06f42-103">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="06f42-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="06f42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06f42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06f42-105">Содержит точечный рисунок значка половинной емкости для формы.</span><span class="sxs-lookup"><span data-stu-id="06f42-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06f42-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="06f42-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06f42-107">ПР_МИНИ_ИКОН</span><span class="sxs-lookup"><span data-stu-id="06f42-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="06f42-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="06f42-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06f42-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="06f42-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="06f42-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="06f42-110">Data type:</span></span>  <br/> |<span data-ttu-id="06f42-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="06f42-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="06f42-112">Область:</span><span class="sxs-lookup"><span data-stu-id="06f42-112">Area:</span></span>  <br/> |<span data-ttu-id="06f42-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="06f42-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f42-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="06f42-114">Remarks</span></span>

<span data-ttu-id="06f42-115">Это свойство содержит изображение значка размером 32 × 32, аналогичное содержимому элемента. ICO, но только верхний левый 16 × 16 пикселя считается существенным.</span><span class="sxs-lookup"><span data-stu-id="06f42-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="06f42-116">Обычно это свойство копируется из. ICO файл, указанный в строке Смалликон соответствующего раздела [Description] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="06f42-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="06f42-117">**Note (Примечание** ) Некоторые платформы не поддерживают 16 × 16 значков пикселей.</span><span class="sxs-lookup"><span data-stu-id="06f42-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="06f42-118">Формат 32 × 32 для этого свойства можно использовать в таком случае, но клиентские приложения должны знать о несоответствиях отображения.</span><span class="sxs-lookup"><span data-stu-id="06f42-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06f42-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="06f42-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06f42-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="06f42-120">Header files</span></span>

<span data-ttu-id="06f42-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="06f42-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="06f42-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="06f42-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="06f42-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="06f42-123">Mapitags.h</span></span>
  
> <span data-ttu-id="06f42-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="06f42-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06f42-125">См. также</span><span class="sxs-lookup"><span data-stu-id="06f42-125">See also</span></span>



[<span data-ttu-id="06f42-126">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="06f42-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="06f42-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06f42-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06f42-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="06f42-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06f42-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="06f42-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06f42-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="06f42-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

