---
title: Каноническое свойство PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c2ddb5da9202e9cf0d1c78da1c1ad085ef9687c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357801"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="0ec46-103">Каноническое свойство PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="0ec46-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="0ec46-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ec46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ec46-105">Указывает, были ли отправлены приглашения на собрание, которое представляет это собрание.</span><span class="sxs-lookup"><span data-stu-id="0ec46-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ec46-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0ec46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ec46-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="0ec46-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="0ec46-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0ec46-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ec46-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0ec46-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0ec46-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0ec46-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ec46-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="0ec46-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="0ec46-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0ec46-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ec46-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0ec46-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0ec46-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0ec46-114">Area:</span></span>  <br/> |<span data-ttu-id="0ec46-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="0ec46-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ec46-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ec46-116">Remarks</span></span>

<span data-ttu-id="0ec46-117">Значение FALSE или отсутствие этого свойства указывает на то, что запрос на собрание никогда не был отправлен.</span><span class="sxs-lookup"><span data-stu-id="0ec46-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="0ec46-118">Значение TRUE указывает, что был отправлен запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="0ec46-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="0ec46-119">После того как это значение заданной для TRUE на собрании, его не следует менять.</span><span class="sxs-lookup"><span data-stu-id="0ec46-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ec46-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0ec46-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ec46-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0ec46-121">Protocol specifications</span></span>

<span data-ttu-id="0ec46-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ec46-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ec46-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0ec46-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ec46-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ec46-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ec46-125">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ec46-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ec46-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0ec46-126">Header files</span></span>

<span data-ttu-id="0ec46-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ec46-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ec46-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0ec46-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ec46-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0ec46-129">See also</span></span>



[<span data-ttu-id="0ec46-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec46-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ec46-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec46-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ec46-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec46-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ec46-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0ec46-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

