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
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355155"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="c5423-103">Каноническое свойство PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="c5423-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="c5423-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5423-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5423-105">Содержит смещение (в символах), используемое для отображения вложения в тексте основного сообщения.</span><span class="sxs-lookup"><span data-stu-id="c5423-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5423-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5423-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5423-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="c5423-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="c5423-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c5423-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5423-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="c5423-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="c5423-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5423-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5423-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c5423-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c5423-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c5423-112">Area:</span></span>  <br/> |<span data-ttu-id="c5423-113">Вложение MAPI</span><span class="sxs-lookup"><span data-stu-id="c5423-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5423-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5423-114">Remarks</span></span>

<span data-ttu-id="c5423-115">Если указанное смещение равно-1 (0xFFFFFFFF), то вложение не отображается с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c5423-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="c5423-116">Все значения, отличные от-1, указывают положение в свойстве **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), в котором будет отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="c5423-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="c5423-117">**Note (Примечание** ) Символ, указанный этим свойством в **PR_BODY** , заменяется вложением.</span><span class="sxs-lookup"><span data-stu-id="c5423-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="c5423-118">Как правило, этот символ является пробелом, хотя также можно использовать специальный замещающий символ.</span><span class="sxs-lookup"><span data-stu-id="c5423-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="c5423-119">Это свойство выражается в символах.</span><span class="sxs-lookup"><span data-stu-id="c5423-119">This property is expressed in characters.</span></span> <span data-ttu-id="c5423-120">В некоторых наборах символов это значение не соответствует байтам.</span><span class="sxs-lookup"><span data-stu-id="c5423-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="c5423-121">Приложения, поддерживающие Юникод, могут вычислять положение на основе двухбайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="c5423-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="c5423-122">Приложения с двухбайтовым набором знаков (DBCS) должны сканировать текст вплоть до значения этого свойства, так как их представление символов зависит от одного до двух байтов на символ.</span><span class="sxs-lookup"><span data-stu-id="c5423-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="c5423-123">Это свойство не следует использовать в тексте в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="c5423-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="c5423-124">Положение отрисовки указывается в формате RTF с помощью escape-последовательности, которая называется заполнителем вложенного объекта.</span><span class="sxs-lookup"><span data-stu-id="c5423-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="c5423-125">Эта последовательность состоит из строки `\objattph` , за которой следует один символ, обычно пробел, который заменяется отрисовкой вложений.</span><span class="sxs-lookup"><span data-stu-id="c5423-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c5423-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5423-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5423-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5423-127">Protocol specifications</span></span>

<span data-ttu-id="c5423-128">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5423-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5423-129">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5423-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5423-130">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5423-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5423-131">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="c5423-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5423-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5423-132">Header files</span></span>

<span data-ttu-id="c5423-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c5423-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5423-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5423-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5423-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c5423-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c5423-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c5423-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5423-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c5423-137">See also</span></span>



[<span data-ttu-id="c5423-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5423-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5423-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c5423-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5423-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5423-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5423-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5423-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

