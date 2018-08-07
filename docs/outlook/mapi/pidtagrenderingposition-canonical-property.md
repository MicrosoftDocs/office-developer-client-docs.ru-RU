---
title: Каноническое свойство PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811709"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="a48cb-103">Каноническое свойство PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="a48cb-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="a48cb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a48cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a48cb-105">Содержит смещение в символы, следует использовать при визуализации вложения в тексте основного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a48cb-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a48cb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a48cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a48cb-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="a48cb-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="a48cb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a48cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a48cb-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="a48cb-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="a48cb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a48cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a48cb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a48cb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a48cb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a48cb-112">Area:</span></span>  <br/> |<span data-ttu-id="a48cb-113">Вложений MAPI</span><span class="sxs-lookup"><span data-stu-id="a48cb-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a48cb-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a48cb-114">Remarks</span></span>

<span data-ttu-id="a48cb-115">Если заданный смещение равно -1 (0xFFFFFFFF), вложение не отображаются с использованием этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a48cb-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="a48cb-116">Все значения, отличные от -1 указывает положение в пределах свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), в которой для отображения вложение.</span><span class="sxs-lookup"><span data-stu-id="a48cb-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="a48cb-117">**Примечание** Символ, указанный в параметре это свойство **PR_BODY** заменяется вложение.</span><span class="sxs-lookup"><span data-stu-id="a48cb-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="a48cb-118">Обычно это пробелами, несмотря на то, что также можно использовать специальный заполнитель.</span><span class="sxs-lookup"><span data-stu-id="a48cb-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="a48cb-119">Это свойство выражается в символы.</span><span class="sxs-lookup"><span data-stu-id="a48cb-119">This property is expressed in characters.</span></span> <span data-ttu-id="a48cb-120">В некоторых наборах знаков, это не лежат в байтах.</span><span class="sxs-lookup"><span data-stu-id="a48cb-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="a48cb-121">Юникод приложений можно вычислить положение, основываясь на двухбайтовых знаков.</span><span class="sxs-lookup"><span data-stu-id="a48cb-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="a48cb-122">Из-за их представление знака может отличаться от одного до двух байт на символ приложений задать двухбайтовых знаков (DBCS) необходимо проверить текста до значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a48cb-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="a48cb-123">Это свойство следует использовать не с текстом форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="a48cb-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="a48cb-124">Положения обозначается escape-последовательность называется заполнитель object вложений в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="a48cb-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="a48cb-125">Эта последовательность включает строку `\objattph` за которой следует один символ, обычно сколько места на диске, будет заменена с отображением вложения.</span><span class="sxs-lookup"><span data-stu-id="a48cb-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a48cb-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a48cb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a48cb-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a48cb-127">Protocol specifications</span></span>

<span data-ttu-id="a48cb-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a48cb-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a48cb-129">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a48cb-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a48cb-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a48cb-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a48cb-131">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="a48cb-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a48cb-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a48cb-132">Header files</span></span>

<span data-ttu-id="a48cb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a48cb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a48cb-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a48cb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a48cb-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a48cb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a48cb-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a48cb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a48cb-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a48cb-137">See also</span></span>



[<span data-ttu-id="a48cb-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a48cb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a48cb-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a48cb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a48cb-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a48cb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a48cb-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a48cb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

