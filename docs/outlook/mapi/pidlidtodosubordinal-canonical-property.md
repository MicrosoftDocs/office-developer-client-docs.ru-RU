---
title: Каноническое свойство PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344921"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="c3d6a-103">Каноническое свойство PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="c3d6a-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="c3d6a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d6a-105">Выступает в качестве разблокера при сортировке объектов **свойством dispidToDoOrdinalDate** [(PidLidToDoOrdinalDate)](pidlidtodoordinaldate-canonical-property.md)и результатом в результате.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3d6a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c3d6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3d6a-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="c3d6a-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="c3d6a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c3d6a-108">Property set:</span></span>  <br/> |<span data-ttu-id="c3d6a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c3d6a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c3d6a-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c3d6a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c3d6a-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="c3d6a-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="c3d6a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c3d6a-112">Data type:</span></span>  <br/> |<span data-ttu-id="c3d6a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c3d6a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c3d6a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c3d6a-114">Area:</span></span>  <br/> |<span data-ttu-id="c3d6a-115">Task</span><span class="sxs-lookup"><span data-stu-id="c3d6a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3d6a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3d6a-116">Remarks</span></span>

<span data-ttu-id="c3d6a-117">Если используется, это свойство должно быть отсортифицировано словарно.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="c3d6a-118">Символы компонента строки должны состоять только из цифр от нуля до девяти.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="c3d6a-119">Изначально этому свойству следует установить "5555555".</span><span class="sxs-lookup"><span data-stu-id="c3d6a-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="c3d6a-120">Длина этого свойства не должна превышать 254 символа (за исключением завершающих символов NULL).</span><span class="sxs-lookup"><span data-stu-id="c3d6a-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3d6a-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c3d6a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3d6a-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c3d6a-122">Protocol specifications</span></span>

<span data-ttu-id="c3d6a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3d6a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3d6a-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3d6a-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3d6a-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3d6a-126">Указывает свойства и операции, связанные с помежкой.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3d6a-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c3d6a-127">Header files</span></span>

<span data-ttu-id="c3d6a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3d6a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3d6a-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c3d6a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3d6a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c3d6a-130">See also</span></span>



[<span data-ttu-id="c3d6a-131">Каноническое свойство PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="c3d6a-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="c3d6a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d6a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3d6a-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d6a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3d6a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d6a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3d6a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c3d6a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

