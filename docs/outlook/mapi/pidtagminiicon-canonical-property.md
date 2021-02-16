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
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="7470f-103">Каноническое свойство PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="7470f-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="7470f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7470f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7470f-105">Содержит толограмму полуразмерного значка формы.</span><span class="sxs-lookup"><span data-stu-id="7470f-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7470f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7470f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7470f-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="7470f-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="7470f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7470f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7470f-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="7470f-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="7470f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7470f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7470f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7470f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7470f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7470f-112">Area:</span></span>  <br/> |<span data-ttu-id="7470f-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="7470f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7470f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7470f-114">Remarks</span></span>

<span data-ttu-id="7470f-115">Это свойство содержит изображение значка размером 32 × 32 пикселя, то же самое, что и содержимое значка. ICO-файл, но только верхний левый 16 × 16 пикселей считается значимым.</span><span class="sxs-lookup"><span data-stu-id="7470f-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="7470f-116">Обычно это свойство копируется из . ICO-файл, указанный в строке SmallIcon соответствующего раздела [Описание] файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="7470f-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="7470f-117">**Примечание** Некоторые платформы не поддерживают значки размером 16 × 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="7470f-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="7470f-118">Формат 32 × 32 этого свойства можно использовать в таком случае, но клиентские приложения должны знать о несоответствиях отображения.</span><span class="sxs-lookup"><span data-stu-id="7470f-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7470f-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7470f-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7470f-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7470f-120">Header files</span></span>

<span data-ttu-id="7470f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7470f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7470f-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7470f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7470f-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7470f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7470f-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7470f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7470f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7470f-125">See also</span></span>



[<span data-ttu-id="7470f-126">Каноническое свойство PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="7470f-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="7470f-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7470f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7470f-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7470f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7470f-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7470f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7470f-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7470f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

