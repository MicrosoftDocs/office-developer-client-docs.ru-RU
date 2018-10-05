---
title: Каноническое свойство PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382472"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="061e4-103">Каноническое свойство PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="061e4-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="061e4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="061e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="061e4-105">Указывает время первоначальной сигнал напоминания.</span><span class="sxs-lookup"><span data-stu-id="061e4-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="061e4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="061e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="061e4-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="061e4-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="061e4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="061e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="061e4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="061e4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="061e4-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="061e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="061e4-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="061e4-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="061e4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="061e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="061e4-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="061e4-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="061e4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="061e4-114">Area:</span></span>  <br/> |<span data-ttu-id="061e4-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="061e4-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="061e4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="061e4-116">Remarks</span></span>

<span data-ttu-id="061e4-117">Для объектов, календарь это свойство представляет время, когда пользователь может быть позднее которого является время начала встречи.</span><span class="sxs-lookup"><span data-stu-id="061e4-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="061e4-118">Клиенты необходимо задать значение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="061e4-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="061e4-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="061e4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="061e4-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="061e4-120">Protocol specifications</span></span>

<span data-ttu-id="061e4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="061e4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="061e4-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="061e4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="061e4-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="061e4-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="061e4-124">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="061e4-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="061e4-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="061e4-125">Header files</span></span>

<span data-ttu-id="061e4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="061e4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="061e4-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="061e4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="061e4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="061e4-128">See also</span></span>



[<span data-ttu-id="061e4-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="061e4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="061e4-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="061e4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="061e4-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="061e4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="061e4-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="061e4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

