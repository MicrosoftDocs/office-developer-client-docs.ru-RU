---
title: Каноническое свойство PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356730"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="ab9e9-103">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="ab9e9-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="ab9e9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab9e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab9e9-105">Содержит толограмму значка полного размера формы.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab9e9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ab9e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab9e9-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="ab9e9-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="ab9e9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ab9e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab9e9-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="ab9e9-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="ab9e9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ab9e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab9e9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ab9e9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ab9e9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ab9e9-112">Area:</span></span>  <br/> |<span data-ttu-id="ab9e9-113">MAPI, не передаваемый</span><span class="sxs-lookup"><span data-stu-id="ab9e9-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab9e9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab9e9-114">Remarks</span></span>

<span data-ttu-id="ab9e9-115">Это свойство содержит изображение значка размером 32 × 32 пикселя, то же самое, что и содержимое значка. ICO-файл.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="ab9e9-116">Обычно это свойство копируется из . ICO-файл, указанный в строке LargeIcon соответствующего раздела [Описание] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab9e9-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ab9e9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab9e9-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ab9e9-118">Protocol specifications</span></span>

<span data-ttu-id="ab9e9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab9e9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab9e9-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab9e9-121">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ab9e9-121">Header files</span></span>

<span data-ttu-id="ab9e9-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab9e9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab9e9-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab9e9-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab9e9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ab9e9-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ab9e9-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab9e9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ab9e9-126">See also</span></span>



[<span data-ttu-id="ab9e9-127">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="ab9e9-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="ab9e9-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ab9e9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab9e9-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ab9e9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab9e9-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ab9e9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab9e9-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ab9e9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

