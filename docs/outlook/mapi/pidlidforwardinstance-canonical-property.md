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
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357773"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="f0f1a-103">Каноническое свойство PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="f0f1a-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="f0f1a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0f1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0f1a-105">Указывает, что запрос собрания представляет собой исключение из повторяющейся серии, и он был перенаправл (даже если он был отправлен организатором), а не приглашением, отправленным организатором.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0f1a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0f1a-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="f0f1a-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="f0f1a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-108">Property set:</span></span>  <br/> |<span data-ttu-id="f0f1a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f0f1a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f0f1a-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f0f1a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f0f1a-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="f0f1a-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="f0f1a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-112">Data type:</span></span>  <br/> |<span data-ttu-id="f0f1a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f0f1a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f0f1a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f0f1a-114">Area:</span></span>  <br/> |<span data-ttu-id="f0f1a-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="f0f1a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0f1a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0f1a-116">Remarks</span></span>

<span data-ttu-id="f0f1a-117">Значение FALSE для этого свойства указывает на то, что запрос собрания не является переадверяемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="f0f1a-118">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0f1a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f0f1a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0f1a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f0f1a-120">Protocol specifications</span></span>

<span data-ttu-id="f0f1a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0f1a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0f1a-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0f1a-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0f1a-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0f1a-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0f1a-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f0f1a-125">Header files</span></span>

<span data-ttu-id="f0f1a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0f1a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0f1a-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f0f1a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0f1a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f0f1a-128">See also</span></span>



[<span data-ttu-id="f0f1a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f1a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0f1a-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f1a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0f1a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f1a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0f1a-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f0f1a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

