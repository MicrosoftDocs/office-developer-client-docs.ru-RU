---
title: Каноническое свойство PidLidForwardInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c32a60c7655f4e468a03013cb3979bde228ea3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810362"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="e7b35-103">Каноническое свойство PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="e7b35-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="e7b35-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7b35-105">Указывает, что запрос на собрание представляет исключение в повторяющееся и переслано (даже если перенаправленные с организатором) а не приглашение принять участие в отправленных организатора.</span><span class="sxs-lookup"><span data-stu-id="e7b35-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7b35-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7b35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7b35-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="e7b35-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="e7b35-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e7b35-108">Property set:</span></span>  <br/> |<span data-ttu-id="e7b35-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e7b35-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e7b35-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="e7b35-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e7b35-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="e7b35-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="e7b35-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7b35-112">Data type:</span></span>  <br/> |<span data-ttu-id="e7b35-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e7b35-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e7b35-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e7b35-114">Area:</span></span>  <br/> |<span data-ttu-id="e7b35-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="e7b35-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7b35-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7b35-116">Remarks</span></span>

<span data-ttu-id="e7b35-117">Значение FALSE для этого свойства указывает, что запрос на собрание не переадресованных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e7b35-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="e7b35-118">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="e7b35-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7b35-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7b35-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7b35-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e7b35-120">Protocol specifications</span></span>

<span data-ttu-id="e7b35-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7b35-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7b35-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e7b35-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7b35-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7b35-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7b35-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="e7b35-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7b35-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7b35-125">Header files</span></span>

<span data-ttu-id="e7b35-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7b35-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7b35-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7b35-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7b35-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e7b35-128">See also</span></span>



[<span data-ttu-id="e7b35-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b35-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7b35-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b35-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7b35-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7b35-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7b35-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7b35-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

