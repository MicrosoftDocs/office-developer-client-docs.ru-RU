---
title: Каноническое свойство PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315892"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="d39f2-103">Каноническое свойство PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="d39f2-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="d39f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d39f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d39f2-105">Задает интервал (в минутах) между моментом, когда напоминание становится просроченным, и время начала объекта Calendar.</span><span class="sxs-lookup"><span data-stu-id="d39f2-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d39f2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d39f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d39f2-107">диспидреминдерделта</span><span class="sxs-lookup"><span data-stu-id="d39f2-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="d39f2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d39f2-108">Property set:</span></span>  <br/> |<span data-ttu-id="d39f2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d39f2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d39f2-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d39f2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d39f2-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="d39f2-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="d39f2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d39f2-112">Data type:</span></span>  <br/> |<span data-ttu-id="d39f2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d39f2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d39f2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d39f2-114">Area:</span></span>  <br/> |<span data-ttu-id="d39f2-115">Напоминание</span><span class="sxs-lookup"><span data-stu-id="d39f2-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d39f2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d39f2-116">Remarks</span></span>

<span data-ttu-id="d39f2-117">Это свойство должно быть задано для объектов календаря.</span><span class="sxs-lookup"><span data-stu-id="d39f2-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="d39f2-118">Для всех объектов, не относящихся к календарю, этому свойству следует присвоить значение "0x00000000" и игнорировать.</span><span class="sxs-lookup"><span data-stu-id="d39f2-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="d39f2-119">При закрытии напоминания для одного экземпляра повторяющегося объекта Calendar значение этого свойства используется при вычислении времени сигнала для следующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d39f2-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="d39f2-120">Сведения о создании объекта Calendar [[MS – оксокал]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d39f2-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d39f2-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d39f2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d39f2-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d39f2-122">Protocol specifications</span></span>

<span data-ttu-id="d39f2-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d39f2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d39f2-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d39f2-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d39f2-125">[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d39f2-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d39f2-126">Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.</span><span class="sxs-lookup"><span data-stu-id="d39f2-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d39f2-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d39f2-127">Header files</span></span>

<span data-ttu-id="d39f2-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d39f2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d39f2-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d39f2-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d39f2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d39f2-130">See also</span></span>



[<span data-ttu-id="d39f2-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d39f2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d39f2-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d39f2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d39f2-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d39f2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d39f2-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d39f2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

