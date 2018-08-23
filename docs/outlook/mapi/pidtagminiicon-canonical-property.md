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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589779"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="eb5b3-103">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="eb5b3-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="eb5b3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb5b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb5b3-105">Содержит растрового изображения значка наполовину размер для формы.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb5b3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eb5b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb5b3-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="eb5b3-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="eb5b3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eb5b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb5b3-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="eb5b3-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="eb5b3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eb5b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb5b3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eb5b3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eb5b3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="eb5b3-112">Area:</span></span>  <br/> |<span data-ttu-id="eb5b3-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="eb5b3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb5b3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb5b3-114">Remarks</span></span>

<span data-ttu-id="eb5b3-115">Это свойство содержит изображение значка, то же, что содержимое в размером 32 на 32 пикселя. Файл ICO, но только верхнем левом углу 16 × 16 пикселей, считаются значительные.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="eb5b3-116">Это свойство обычно копируются из. ICO-файла, указанного в строке SmallIcon соответствующий раздел [Описание] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="eb5b3-117">**Примечание** Некоторые платформы выполните не значки поддержки 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="eb5b3-118">Формат размером 32 на 32 это свойство можно использовать в таком случае, но клиентские приложения следует иметь в виду несоответствия отображения.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eb5b3-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb5b3-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eb5b3-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="eb5b3-120">Header files</span></span>

<span data-ttu-id="eb5b3-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb5b3-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb5b3-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb5b3-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb5b3-123">Mapitags.h</span></span>
  
> <span data-ttu-id="eb5b3-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="eb5b3-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb5b3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="eb5b3-125">See also</span></span>



[<span data-ttu-id="eb5b3-126">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="eb5b3-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="eb5b3-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb5b3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb5b3-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb5b3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb5b3-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eb5b3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb5b3-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eb5b3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

