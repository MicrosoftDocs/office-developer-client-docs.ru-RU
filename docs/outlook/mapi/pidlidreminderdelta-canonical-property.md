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
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="ede49-103">Каноническое свойство PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="ede49-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="ede49-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ede49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ede49-105">Указывает интервал (в минутах) между временем первого просрочения напоминания и временем начала объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="ede49-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ede49-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ede49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ede49-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="ede49-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="ede49-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ede49-108">Property set:</span></span>  <br/> |<span data-ttu-id="ede49-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ede49-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ede49-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ede49-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ede49-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="ede49-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="ede49-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ede49-112">Data type:</span></span>  <br/> |<span data-ttu-id="ede49-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ede49-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ede49-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ede49-114">Area:</span></span>  <br/> |<span data-ttu-id="ede49-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="ede49-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ede49-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ede49-116">Remarks</span></span>

<span data-ttu-id="ede49-117">Это свойство должно быть установлено для объектов календаря.</span><span class="sxs-lookup"><span data-stu-id="ede49-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="ede49-118">Для всех объектов, не относяхся к календарю, это свойство должно иметь 0x00000000 и игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ede49-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="ede49-119">При отклонении напоминания для одного экземпляра повторяющегося объекта календаря значение этого свойства используется при вычислении времени сигнала для следующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ede49-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="ede49-120">Подробные сведения о создании объекта календаря см. в [[MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ede49-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ede49-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ede49-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ede49-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ede49-122">Protocol specifications</span></span>

<span data-ttu-id="ede49-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ede49-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ede49-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="ede49-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ede49-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ede49-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ede49-126">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний об объектах.</span><span class="sxs-lookup"><span data-stu-id="ede49-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ede49-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ede49-127">Header files</span></span>

<span data-ttu-id="ede49-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ede49-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ede49-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ede49-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ede49-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ede49-130">See also</span></span>



[<span data-ttu-id="ede49-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ede49-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ede49-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ede49-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ede49-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ede49-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ede49-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ede49-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

