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
ms.openlocfilehash: 91cad169157b2dd0ff279e88b69db149c4c7df89
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590752"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="4c6ab-103">Каноническое свойство PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="4c6ab-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="4c6ab-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c6ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c6ab-105">Указывает интервал в минутах между времени, когда напоминания сначала становится просроченные и время начала объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c6ab-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4c6ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c6ab-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="4c6ab-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="4c6ab-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4c6ab-108">Property set:</span></span>  <br/> |<span data-ttu-id="4c6ab-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4c6ab-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4c6ab-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4c6ab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4c6ab-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="4c6ab-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="4c6ab-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4c6ab-112">Data type:</span></span>  <br/> |<span data-ttu-id="4c6ab-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4c6ab-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4c6ab-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4c6ab-114">Area:</span></span>  <br/> |<span data-ttu-id="4c6ab-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="4c6ab-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c6ab-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4c6ab-116">Remarks</span></span>

<span data-ttu-id="4c6ab-117">Это свойство необходимо установить на объекты календаря.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="4c6ab-118">Для всех объектов не календаря это свойство должно иметь значение «0x00000000» и будет пропущен.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="4c6ab-119">После закрытия напоминания для одного экземпляра объекта повторяющихся календаря, значение этого свойства используется в расчет времени сигнала следующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="4c6ab-120">Для получения дополнительных сведений о создании объекта календаря в разделе [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4c6ab-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c6ab-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4c6ab-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c6ab-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4c6ab-122">Protocol specifications</span></span>

<span data-ttu-id="4c6ab-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c6ab-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c6ab-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c6ab-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c6ab-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c6ab-126">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c6ab-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4c6ab-127">Header files</span></span>

<span data-ttu-id="4c6ab-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c6ab-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c6ab-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4c6ab-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c6ab-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4c6ab-130">See also</span></span>



[<span data-ttu-id="4c6ab-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4c6ab-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c6ab-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4c6ab-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c6ab-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4c6ab-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c6ab-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4c6ab-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

