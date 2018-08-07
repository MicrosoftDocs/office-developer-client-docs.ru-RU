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
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811383"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="98dbc-103">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="98dbc-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="98dbc-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98dbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98dbc-105">Содержит растрового изображения значка наполовину размер для формы.</span><span class="sxs-lookup"><span data-stu-id="98dbc-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98dbc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="98dbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98dbc-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="98dbc-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="98dbc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="98dbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98dbc-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="98dbc-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="98dbc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="98dbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="98dbc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98dbc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98dbc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="98dbc-112">Area:</span></span>  <br/> |<span data-ttu-id="98dbc-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="98dbc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98dbc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="98dbc-114">Remarks</span></span>

<span data-ttu-id="98dbc-115">Это свойство содержит изображение значка, то же, что содержимое в размером 32 на 32 пикселя. Файл ICO, но только верхнем левом углу 16 × 16 пикселей, считаются значительные.</span><span class="sxs-lookup"><span data-stu-id="98dbc-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="98dbc-116">Это свойство обычно копируются из. ICO-файла, указанного в строке SmallIcon соответствующий раздел [Описание] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="98dbc-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="98dbc-117">**Примечание** Некоторые платформы выполните не значки поддержки 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="98dbc-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="98dbc-118">Формат размером 32 на 32 это свойство можно использовать в таком случае, но клиентские приложения следует иметь в виду несоответствия отображения.</span><span class="sxs-lookup"><span data-stu-id="98dbc-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98dbc-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98dbc-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="98dbc-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="98dbc-120">Header files</span></span>

<span data-ttu-id="98dbc-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98dbc-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="98dbc-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="98dbc-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="98dbc-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98dbc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="98dbc-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="98dbc-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98dbc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="98dbc-125">See also</span></span>



[<span data-ttu-id="98dbc-126">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="98dbc-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="98dbc-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98dbc-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98dbc-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98dbc-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98dbc-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="98dbc-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98dbc-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="98dbc-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

