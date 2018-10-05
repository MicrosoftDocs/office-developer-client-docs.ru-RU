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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384565"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="032ea-103">Каноническое свойство PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="032ea-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="032ea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="032ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="032ea-105">Действует как средства разбиения слов связывают при свойство **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) сортирует объекты и результатов в набор функций.</span><span class="sxs-lookup"><span data-stu-id="032ea-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="032ea-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="032ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="032ea-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="032ea-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="032ea-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="032ea-108">Property set:</span></span>  <br/> |<span data-ttu-id="032ea-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="032ea-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="032ea-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="032ea-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="032ea-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="032ea-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="032ea-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="032ea-112">Data type:</span></span>  <br/> |<span data-ttu-id="032ea-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="032ea-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="032ea-114">Область:</span><span class="sxs-lookup"><span data-stu-id="032ea-114">Area:</span></span>  <br/> |<span data-ttu-id="032ea-115">Task</span><span class="sxs-lookup"><span data-stu-id="032ea-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="032ea-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="032ea-116">Remarks</span></span>

<span data-ttu-id="032ea-117">При использовании этого свойства должны быть отсортированы lexicographically.</span><span class="sxs-lookup"><span data-stu-id="032ea-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="032ea-118">Компонент символов строки должен содержать только цифры нулевой до девяти.</span><span class="sxs-lookup"><span data-stu-id="032ea-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="032ea-119">Это свойство необходимо сначала задать «5555555».</span><span class="sxs-lookup"><span data-stu-id="032ea-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="032ea-120">Длина этого свойства не должна превышать 254 символов (не включая конечный НУЛЕВОЙ символ).</span><span class="sxs-lookup"><span data-stu-id="032ea-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="032ea-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="032ea-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="032ea-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="032ea-122">Protocol specifications</span></span>

<span data-ttu-id="032ea-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032ea-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032ea-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="032ea-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="032ea-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032ea-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032ea-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="032ea-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="032ea-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="032ea-127">Header files</span></span>

<span data-ttu-id="032ea-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="032ea-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="032ea-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="032ea-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="032ea-130">См. также</span><span class="sxs-lookup"><span data-stu-id="032ea-130">See also</span></span>



[<span data-ttu-id="032ea-131">Каноническое свойство PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="032ea-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="032ea-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="032ea-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="032ea-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="032ea-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="032ea-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="032ea-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="032ea-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="032ea-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

