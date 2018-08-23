---
title: Каноническое свойство PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1a725583faf13fe8b46616d9d341798298a8b53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563438"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="d22c9-103">Каноническое свойство PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="d22c9-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="d22c9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d22c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d22c9-105">Указывает точку времени, когда напоминание переходит из ожидающих просроченные.</span><span class="sxs-lookup"><span data-stu-id="d22c9-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d22c9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d22c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d22c9-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="d22c9-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="d22c9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d22c9-108">Property set:</span></span>  <br/> |<span data-ttu-id="d22c9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d22c9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d22c9-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d22c9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d22c9-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="d22c9-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="d22c9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d22c9-112">Data type:</span></span>  <br/> |<span data-ttu-id="d22c9-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d22c9-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d22c9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d22c9-114">Area:</span></span>  <br/> |<span data-ttu-id="d22c9-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="d22c9-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d22c9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d22c9-116">Remarks</span></span>

<span data-ttu-id="d22c9-117">Это свойство необходимо задать, если свойство **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="d22c9-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="d22c9-118">Клиенты необходимо задать значение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d22c9-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d22c9-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d22c9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d22c9-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d22c9-120">Protocol specifications</span></span>

<span data-ttu-id="d22c9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d22c9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d22c9-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d22c9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d22c9-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d22c9-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d22c9-124">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="d22c9-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d22c9-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d22c9-125">Header files</span></span>

<span data-ttu-id="d22c9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d22c9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d22c9-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d22c9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d22c9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d22c9-128">See also</span></span>



[<span data-ttu-id="d22c9-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d22c9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d22c9-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d22c9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d22c9-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d22c9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d22c9-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d22c9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

