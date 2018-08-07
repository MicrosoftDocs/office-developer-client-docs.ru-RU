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
ms.openlocfilehash: e2caccf3cf6ca7e6f15bed1c901d4dfbb198f19b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810480"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="a0fa3-103">Каноническое свойство PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="a0fa3-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="a0fa3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0fa3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0fa3-105">Указывает интервал в минутах между времени, когда напоминания сначала становится просроченные и время начала объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0fa3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a0fa3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0fa3-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="a0fa3-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="a0fa3-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a0fa3-108">Property set:</span></span>  <br/> |<span data-ttu-id="a0fa3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a0fa3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a0fa3-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a0fa3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a0fa3-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="a0fa3-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="a0fa3-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a0fa3-112">Data type:</span></span>  <br/> |<span data-ttu-id="a0fa3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0fa3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0fa3-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a0fa3-114">Area:</span></span>  <br/> |<span data-ttu-id="a0fa3-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="a0fa3-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0fa3-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0fa3-116">Remarks</span></span>

<span data-ttu-id="a0fa3-117">Это свойство необходимо установить на объекты календаря.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="a0fa3-118">Для всех объектов не календаря это свойство должно иметь значение «0x00000000» и будет пропущен.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="a0fa3-119">После закрытия напоминания для одного экземпляра объекта повторяющихся календаря, значение этого свойства используется в расчет времени сигнала следующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="a0fa3-120">Для получения дополнительных сведений о создании объекта календаря в разделе [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a0fa3-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0fa3-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0fa3-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0fa3-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a0fa3-122">Protocol specifications</span></span>

<span data-ttu-id="a0fa3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0fa3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0fa3-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0fa3-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0fa3-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0fa3-126">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0fa3-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a0fa3-127">Header files</span></span>

<span data-ttu-id="a0fa3-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0fa3-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0fa3-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a0fa3-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0fa3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a0fa3-130">See also</span></span>



[<span data-ttu-id="a0fa3-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fa3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0fa3-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fa3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0fa3-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fa3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0fa3-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a0fa3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

