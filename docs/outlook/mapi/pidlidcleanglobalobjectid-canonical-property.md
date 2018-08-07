---
title: Каноническое свойство PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a784c91a04cce572c8e30085b1760c28296a1d53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19810238"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="b249c-103">Каноническое свойство PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="b249c-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="b249c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b249c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b249c-105">Задает clean глобального **ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="b249c-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b249c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b249c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b249c-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="b249c-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="b249c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b249c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b249c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="b249c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="b249c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b249c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b249c-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="b249c-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="b249c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b249c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b249c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b249c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b249c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b249c-114">Area:</span></span>  <br/> |<span data-ttu-id="b249c-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="b249c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b249c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b249c-116">Remarks</span></span>

<span data-ttu-id="b249c-117">Формат этого свойства совпадает с, **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b249c-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="b249c-118">Значение этого свойства должно быть равно значению **LID_GLOBAL_OBJID**, за исключением YH, YL, M, а D поля должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b249c-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="b249c-119">Все объекты, которые ссылаются на экземпляр повторяющегося ряда (в том числе потерянного экземпляра), а также ряд повторяющейся, будут иметь такое же значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b249c-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b249c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b249c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b249c-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b249c-121">Protocol specifications</span></span>

<span data-ttu-id="b249c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b249c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b249c-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b249c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b249c-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b249c-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b249c-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="b249c-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b249c-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b249c-126">Header files</span></span>

<span data-ttu-id="b249c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b249c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b249c-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b249c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b249c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b249c-129">See also</span></span>



[<span data-ttu-id="b249c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b249c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b249c-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b249c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b249c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b249c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b249c-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b249c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

