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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358711"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="8ce06-103">Каноническое свойство PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="8ce06-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="8ce06-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ce06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ce06-105">Указывает начальное время сигнала для напоминания.</span><span class="sxs-lookup"><span data-stu-id="8ce06-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ce06-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ce06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ce06-107">диспидреминдертиме</span><span class="sxs-lookup"><span data-stu-id="8ce06-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="8ce06-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8ce06-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ce06-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8ce06-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8ce06-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8ce06-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ce06-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="8ce06-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="8ce06-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ce06-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ce06-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8ce06-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8ce06-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8ce06-114">Area:</span></span>  <br/> |<span data-ttu-id="8ce06-115">Напоминание</span><span class="sxs-lookup"><span data-stu-id="8ce06-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ce06-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ce06-116">Remarks</span></span>

<span data-ttu-id="8ce06-117">Для объектов Calendar это свойство представляет время, когда пользователь будет заменяться временем начала встречи.</span><span class="sxs-lookup"><span data-stu-id="8ce06-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="8ce06-118">Клиенты должны задать значение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="8ce06-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8ce06-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ce06-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ce06-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ce06-120">Protocol specifications</span></span>

<span data-ttu-id="8ce06-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ce06-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ce06-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ce06-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ce06-123">[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ce06-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ce06-124">Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.</span><span class="sxs-lookup"><span data-stu-id="8ce06-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ce06-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8ce06-125">Header files</span></span>

<span data-ttu-id="8ce06-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8ce06-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ce06-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ce06-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ce06-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8ce06-128">See also</span></span>



[<span data-ttu-id="8ce06-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce06-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ce06-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce06-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ce06-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce06-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ce06-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ce06-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

