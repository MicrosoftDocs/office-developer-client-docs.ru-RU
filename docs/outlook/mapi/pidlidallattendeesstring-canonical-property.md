---
title: Каноническое свойство PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96ad0727797475effd0563e4753070cb3bac4b37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334778"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="9878b-103">Каноническое свойство PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="9878b-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="9878b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9878b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9878b-105">Указывает список всех участников, кроме организатора, включая ресурсы и неисключаемых участников.</span><span class="sxs-lookup"><span data-stu-id="9878b-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9878b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9878b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9878b-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="9878b-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="9878b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9878b-108">Property set:</span></span>  <br/> |<span data-ttu-id="9878b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="9878b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9878b-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="9878b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9878b-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="9878b-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="9878b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9878b-112">Data type:</span></span>  <br/> |<span data-ttu-id="9878b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9878b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9878b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9878b-114">Area:</span></span>  <br/> |<span data-ttu-id="9878b-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="9878b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9878b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9878b-116">Remarks</span></span>

<span data-ttu-id="9878b-117">Значением для каждого участника является отображаемая фамилия участника.</span><span class="sxs-lookup"><span data-stu-id="9878b-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="9878b-118">Разделимые записи должны разделяться за осью с заосью, за которой следует пробел.</span><span class="sxs-lookup"><span data-stu-id="9878b-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="9878b-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="9878b-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9878b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9878b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9878b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9878b-121">Protocol specifications</span></span>

<span data-ttu-id="9878b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9878b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9878b-123">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="9878b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9878b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9878b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9878b-125">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9878b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9878b-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="9878b-126">Header files</span></span>

<span data-ttu-id="9878b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9878b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9878b-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9878b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9878b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9878b-129">See also</span></span>



[<span data-ttu-id="9878b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9878b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9878b-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9878b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9878b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9878b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9878b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9878b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

