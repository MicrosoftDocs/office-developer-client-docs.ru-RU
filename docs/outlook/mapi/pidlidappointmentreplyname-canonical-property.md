---
title: Каноническое свойство PidLidAppointmentReplyName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387981"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="6a054-103">Каноническое свойство PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="6a054-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="6a054-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a054-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a054-105">Указывает пользователя, который последнего дан ответ на запрос на собрание или собрания обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="6a054-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a054-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6a054-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a054-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="6a054-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="6a054-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6a054-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a054-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6a054-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6a054-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="6a054-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6a054-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="6a054-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="6a054-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6a054-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a054-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a054-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a054-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6a054-114">Area:</span></span>  <br/> |<span data-ttu-id="6a054-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="6a054-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a054-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a054-116">Remarks</span></span>

<span data-ttu-id="6a054-117">Это свойство устанавливается только для сотрудника, когда ответил делегата.</span><span class="sxs-lookup"><span data-stu-id="6a054-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="6a054-118">Значение равно свойству **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) для хранения делегата.</span><span class="sxs-lookup"><span data-stu-id="6a054-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="6a054-119">Это свойство не имеет значения для организатора.</span><span class="sxs-lookup"><span data-stu-id="6a054-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="6a054-120">Дополнительные сведения о **PR_MAILBOX_OWNER_NAME**см хранения объектов протокола, указанного в [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6a054-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a054-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6a054-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a054-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6a054-122">Protocol specifications</span></span>

<span data-ttu-id="6a054-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a054-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a054-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a054-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a054-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a054-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a054-126">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6a054-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a054-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a054-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a054-128">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="6a054-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a054-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6a054-129">Header files</span></span>

<span data-ttu-id="6a054-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a054-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a054-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a054-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a054-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6a054-132">See also</span></span>



[<span data-ttu-id="6a054-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a054-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a054-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a054-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a054-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6a054-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a054-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6a054-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

