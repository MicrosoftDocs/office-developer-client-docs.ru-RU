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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405417"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="a35ea-103">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="a35ea-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="a35ea-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a35ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a35ea-105">Содержит битовую карту значка размером в полразмера для формы.</span><span class="sxs-lookup"><span data-stu-id="a35ea-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a35ea-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a35ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a35ea-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="a35ea-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="a35ea-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a35ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a35ea-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="a35ea-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="a35ea-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a35ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="a35ea-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a35ea-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a35ea-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a35ea-112">Area:</span></span>  <br/> |<span data-ttu-id="a35ea-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="a35ea-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a35ea-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a35ea-114">Remarks</span></span>

<span data-ttu-id="a35ea-115">Это свойство содержит 32× 32 пиксельного изображения значка, то же самое, что и содержимое . ICO-файл, но только верхние левые 16 × 16 пикселей считаются значительными.</span><span class="sxs-lookup"><span data-stu-id="a35ea-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="a35ea-116">Это свойство обычно копируется из . ICO-файл, указанный в строке SmallIcon соответствующего раздела [Описание] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="a35ea-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="a35ea-117">**Примечание** Некоторые платформы не поддерживают значки 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="a35ea-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="a35ea-118">Формат 32 × 32 этого свойства в таком случае можно использовать, но клиентские приложения должны знать о несоответствиях отображения.</span><span class="sxs-lookup"><span data-stu-id="a35ea-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a35ea-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a35ea-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a35ea-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a35ea-120">Header files</span></span>

<span data-ttu-id="a35ea-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a35ea-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a35ea-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a35ea-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a35ea-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a35ea-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a35ea-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a35ea-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a35ea-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a35ea-125">See also</span></span>



[<span data-ttu-id="a35ea-126">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="a35ea-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="a35ea-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a35ea-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a35ea-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a35ea-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a35ea-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a35ea-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a35ea-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a35ea-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

