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
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400798"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="ff403-103">Каноническое свойство PidTagNull</span><span class="sxs-lookup"><span data-stu-id="ff403-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="ff403-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff403-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff403-105">Представляет значение null или параметры свойства или резервирует массива.</span><span class="sxs-lookup"><span data-stu-id="ff403-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff403-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ff403-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff403-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="ff403-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="ff403-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ff403-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff403-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="ff403-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="ff403-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ff403-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff403-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="ff403-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="ff403-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ff403-112">Area:</span></span>  <br/> |<span data-ttu-id="ff403-113">Common</span><span class="sxs-lookup"><span data-stu-id="ff403-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff403-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ff403-114">Remarks</span></span>

<span data-ttu-id="ff403-115">Это свойство используется для сохранения места в массивах структур [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="ff403-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="ff403-116">Используется в массив структур [SPropTagArray](sproptagarray.md) определить метод для сохранения места в возвращаемый массив структур **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="ff403-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="ff403-117">Это позволяет вычисленные свойства следует реализовать в недорогим способом.</span><span class="sxs-lookup"><span data-stu-id="ff403-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="ff403-118">Для получения дополнительных сведений см [MAPI свойство типа](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ff403-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff403-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ff403-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff403-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ff403-120">Protocol specifications</span></span>

<span data-ttu-id="ff403-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff403-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff403-122">Задает свойства и операции, допустимые на контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="ff403-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff403-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ff403-123">Header files</span></span>

<span data-ttu-id="ff403-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff403-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff403-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ff403-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff403-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff403-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ff403-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ff403-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff403-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ff403-128">See also</span></span>



[<span data-ttu-id="ff403-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff403-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff403-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff403-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff403-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ff403-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff403-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ff403-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

