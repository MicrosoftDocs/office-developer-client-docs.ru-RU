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
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="31715-103">Каноническое свойство PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="31715-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="31715-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31715-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31715-105">Содержит смещение (в символах) для отображения вложения в основном тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="31715-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31715-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="31715-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31715-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="31715-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="31715-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="31715-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31715-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="31715-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="31715-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="31715-110">Data type:</span></span>  <br/> |<span data-ttu-id="31715-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="31715-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="31715-112">Область:</span><span class="sxs-lookup"><span data-stu-id="31715-112">Area:</span></span>  <br/> |<span data-ttu-id="31715-113">Вложение MAPI</span><span class="sxs-lookup"><span data-stu-id="31715-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31715-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="31715-114">Remarks</span></span>

<span data-ttu-id="31715-115">Если предоставленное смещение составляет -1 (0xFFFFFFFF), вложение не отрисовка с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="31715-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="31715-116">Все значения, кроме -1, указывают положение в свойстве **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)в котором должно быть отрисовлено вложение.</span><span class="sxs-lookup"><span data-stu-id="31715-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="31715-117">**Примечание** Символ, указанный этим свойством **в** PR_BODY заменяется вложением.</span><span class="sxs-lookup"><span data-stu-id="31715-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="31715-118">Обычно этот символ является пробелом, хотя также можно использовать специальный замеделя.</span><span class="sxs-lookup"><span data-stu-id="31715-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="31715-119">Это свойство выражается символами.</span><span class="sxs-lookup"><span data-stu-id="31715-119">This property is expressed in characters.</span></span> <span data-ttu-id="31715-120">В некоторых наборах символов это не эквивалентно ветвям.</span><span class="sxs-lookup"><span data-stu-id="31715-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="31715-121">Приложения Юникод могут вычислять положение на основе двух byte символов.</span><span class="sxs-lookup"><span data-stu-id="31715-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="31715-122">Double-Byte приложения набора символов (DBCS) должны сканировать текст до значения этого свойства, так как их представление символов зависит от одного или двухбайт на символ.</span><span class="sxs-lookup"><span data-stu-id="31715-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="31715-123">Это свойство не должно использоваться с текстом RTF.</span><span class="sxs-lookup"><span data-stu-id="31715-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="31715-124">Положение отрисовки указывается в RTF escape-последовательностью, называемой местом вложения объекта.</span><span class="sxs-lookup"><span data-stu-id="31715-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="31715-125">Эта последовательность состоит из строки, за которой следует один символ, обычно пробел, который будет заменен визуализацией  `\objattph` вложения.</span><span class="sxs-lookup"><span data-stu-id="31715-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31715-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31715-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31715-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="31715-127">Protocol specifications</span></span>

<span data-ttu-id="31715-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31715-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31715-129">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="31715-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31715-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31715-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31715-131">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="31715-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31715-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="31715-132">Header files</span></span>

<span data-ttu-id="31715-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31715-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="31715-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="31715-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="31715-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31715-135">Mapitags.h</span></span>
  
> <span data-ttu-id="31715-136">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="31715-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31715-137">См. также</span><span class="sxs-lookup"><span data-stu-id="31715-137">See also</span></span>



[<span data-ttu-id="31715-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="31715-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31715-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="31715-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31715-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="31715-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31715-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="31715-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

