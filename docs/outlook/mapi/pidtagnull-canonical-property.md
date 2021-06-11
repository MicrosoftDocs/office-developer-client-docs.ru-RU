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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329269"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="70190-103">Каноническое свойство PidTagNull</span><span class="sxs-lookup"><span data-stu-id="70190-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="70190-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70190-105">Представляет значение null или параметр пространства массива свойств или резервов.</span><span class="sxs-lookup"><span data-stu-id="70190-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70190-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="70190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70190-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="70190-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="70190-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="70190-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70190-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="70190-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="70190-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="70190-110">Data type:</span></span>  <br/> |<span data-ttu-id="70190-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="70190-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="70190-112">Область:</span><span class="sxs-lookup"><span data-stu-id="70190-112">Area:</span></span>  <br/> |<span data-ttu-id="70190-113">Распространенная</span><span class="sxs-lookup"><span data-stu-id="70190-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70190-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="70190-114">Remarks</span></span>

<span data-ttu-id="70190-115">Это свойство используется для резерва пространства в массивах [структур SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="70190-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="70190-116">Он используется в массиве [структур SPropTagArray,](sproptagarray.md) чтобы сообщить методу, чтобы зарезервировать пространство в возвращаемом массиве **структур SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="70190-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="70190-117">Это позволяет недорого заполнять вычислительные свойства.</span><span class="sxs-lookup"><span data-stu-id="70190-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="70190-118">Дополнительные сведения см. в обзоре типов [свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="70190-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70190-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="70190-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70190-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="70190-120">Protocol specifications</span></span>

<span data-ttu-id="70190-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70190-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70190-122">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="70190-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70190-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="70190-123">Header files</span></span>

<span data-ttu-id="70190-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70190-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="70190-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="70190-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="70190-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70190-126">Mapitags.h</span></span>
  
> <span data-ttu-id="70190-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="70190-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70190-128">См. также</span><span class="sxs-lookup"><span data-stu-id="70190-128">See also</span></span>



[<span data-ttu-id="70190-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70190-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70190-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70190-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70190-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="70190-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70190-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="70190-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

