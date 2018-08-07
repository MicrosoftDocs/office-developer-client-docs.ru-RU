---
title: Каноническое свойство PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55db507055692c9e929b0125abf719d8c03ac967
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811416"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="a7a1e-103">Каноническое свойство PidTagNull</span><span class="sxs-lookup"><span data-stu-id="a7a1e-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="a7a1e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7a1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7a1e-105">Представляет значение null или параметры свойства или резервирует массива.</span><span class="sxs-lookup"><span data-stu-id="a7a1e-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7a1e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a7a1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7a1e-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="a7a1e-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="a7a1e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a7a1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7a1e-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="a7a1e-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="a7a1e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a7a1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7a1e-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="a7a1e-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="a7a1e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a7a1e-112">Area:</span></span>  <br/> |<span data-ttu-id="a7a1e-113">Common</span><span class="sxs-lookup"><span data-stu-id="a7a1e-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7a1e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7a1e-114">Remarks</span></span>

<span data-ttu-id="a7a1e-115">Это свойство используется для сохранения места в массивах структур [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a1e-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="a7a1e-116">Используется в массив структур [SPropTagArray](sproptagarray.md) определить метод для сохранения места в возвращаемый массив структур **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="a7a1e-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="a7a1e-117">Это позволяет вычисленные свойства следует реализовать в недорогим способом.</span><span class="sxs-lookup"><span data-stu-id="a7a1e-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="a7a1e-118">Для получения дополнительных сведений см [MAPI свойство типа](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a7a1e-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7a1e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7a1e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7a1e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a7a1e-120">Protocol specifications</span></span>

<span data-ttu-id="a7a1e-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7a1e-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7a1e-122">Задает свойства и операции, допустимые на контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="a7a1e-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7a1e-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a7a1e-123">Header files</span></span>

<span data-ttu-id="a7a1e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7a1e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7a1e-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a7a1e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7a1e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7a1e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a7a1e-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a7a1e-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7a1e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a7a1e-128">See also</span></span>



[<span data-ttu-id="a7a1e-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7a1e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7a1e-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7a1e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7a1e-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a7a1e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7a1e-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a7a1e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

