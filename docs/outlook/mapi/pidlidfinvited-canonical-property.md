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
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="88006-103">Каноническое свойство PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="88006-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="88006-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88006-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88006-105">Указывает, были ли отправлены приглашения на собрание, которое представляет это собрание.</span><span class="sxs-lookup"><span data-stu-id="88006-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88006-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="88006-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88006-107">диспидфинвитед</span><span class="sxs-lookup"><span data-stu-id="88006-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="88006-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="88006-108">Property set:</span></span>  <br/> |<span data-ttu-id="88006-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="88006-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="88006-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="88006-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88006-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="88006-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="88006-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="88006-112">Data type:</span></span>  <br/> |<span data-ttu-id="88006-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="88006-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="88006-114">Область:</span><span class="sxs-lookup"><span data-stu-id="88006-114">Area:</span></span>  <br/> |<span data-ttu-id="88006-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="88006-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88006-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="88006-116">Remarks</span></span>

<span data-ttu-id="88006-117">Значение FALSE или отсутствие этого свойства указывает на то, что приглашение на собрание никогда не было отправлено.</span><span class="sxs-lookup"><span data-stu-id="88006-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="88006-118">Значение TRUE указывает, что приглашение на собрание было отправлено.</span><span class="sxs-lookup"><span data-stu-id="88006-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="88006-119">Если для собрания задано значение TRUE, оно не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="88006-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88006-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="88006-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88006-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="88006-121">Protocol specifications</span></span>

<span data-ttu-id="88006-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88006-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88006-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="88006-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88006-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88006-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88006-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="88006-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88006-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="88006-126">Header files</span></span>

<span data-ttu-id="88006-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="88006-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="88006-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="88006-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88006-129">См. также</span><span class="sxs-lookup"><span data-stu-id="88006-129">See also</span></span>



[<span data-ttu-id="88006-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88006-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88006-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="88006-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88006-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="88006-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88006-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="88006-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

