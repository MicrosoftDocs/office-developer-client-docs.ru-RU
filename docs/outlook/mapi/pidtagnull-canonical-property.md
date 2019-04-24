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
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="38e99-103">Каноническое свойство PidTagNull</span><span class="sxs-lookup"><span data-stu-id="38e99-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="38e99-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38e99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38e99-105">Представляет значение null или значение свойства или резервирует пространство массива.</span><span class="sxs-lookup"><span data-stu-id="38e99-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38e99-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="38e99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38e99-107">ПР_НУЛЛ</span><span class="sxs-lookup"><span data-stu-id="38e99-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="38e99-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="38e99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38e99-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="38e99-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="38e99-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="38e99-110">Data type:</span></span>  <br/> |<span data-ttu-id="38e99-111">ПТ_НУЛЛ</span><span class="sxs-lookup"><span data-stu-id="38e99-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="38e99-112">Область:</span><span class="sxs-lookup"><span data-stu-id="38e99-112">Area:</span></span>  <br/> |<span data-ttu-id="38e99-113">Распространенная</span><span class="sxs-lookup"><span data-stu-id="38e99-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38e99-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38e99-114">Remarks</span></span>

<span data-ttu-id="38e99-115">Это свойство используется для резервного места в массивах структур [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="38e99-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="38e99-116">Он используется в массиве структур [спроптагаррай](sproptagarray.md) , чтобы сообщить методу зарезервировать место в возвращенном массиве структур **спропвалуе** .</span><span class="sxs-lookup"><span data-stu-id="38e99-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="38e99-117">Благодаря этому вычисляемые свойства можно заполнять недорогым образом.</span><span class="sxs-lookup"><span data-stu-id="38e99-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="38e99-118">Дополнительные сведения [: Обзор типов свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="38e99-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38e99-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="38e99-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38e99-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="38e99-120">Protocol specifications</span></span>

<span data-ttu-id="38e99-121">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38e99-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38e99-122">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="38e99-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38e99-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="38e99-123">Header files</span></span>

<span data-ttu-id="38e99-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="38e99-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="38e99-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="38e99-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="38e99-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="38e99-126">Mapitags.h</span></span>
  
> <span data-ttu-id="38e99-127">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="38e99-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38e99-128">См. также</span><span class="sxs-lookup"><span data-stu-id="38e99-128">See also</span></span>



[<span data-ttu-id="38e99-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="38e99-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38e99-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="38e99-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38e99-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="38e99-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38e99-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="38e99-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

