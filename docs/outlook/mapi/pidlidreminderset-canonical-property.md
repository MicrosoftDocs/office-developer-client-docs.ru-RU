---
title: Каноническое свойство PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335156"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="94de5-103">Каноническое свойство PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="94de5-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="94de5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94de5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94de5-105">Указывает, установлено ли напоминание для объекта.</span><span class="sxs-lookup"><span data-stu-id="94de5-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94de5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="94de5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94de5-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="94de5-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="94de5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="94de5-108">Property set:</span></span>  <br/> |<span data-ttu-id="94de5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="94de5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="94de5-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="94de5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="94de5-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="94de5-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="94de5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="94de5-112">Data type:</span></span>  <br/> |<span data-ttu-id="94de5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="94de5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="94de5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="94de5-114">Area:</span></span>  <br/> |<span data-ttu-id="94de5-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="94de5-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94de5-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="94de5-116">Remarks</span></span>

<span data-ttu-id="94de5-117">Если для повторяющегося объекта календаря этому свойству задано значение TRUE, клиент может переопредить это значение для исключений.</span><span class="sxs-lookup"><span data-stu-id="94de5-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="94de5-118">Если для повторяющегося объекта календаря это свойство имеет false, напоминания отключаются для всего ряда, включая исключения.</span><span class="sxs-lookup"><span data-stu-id="94de5-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="94de5-119">Для повторяющихся объектов задач это свойство не может быть переопределено исключениями (подробные сведения см. в [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) и [[MS-OXOTASK]).](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94de5-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94de5-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94de5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94de5-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="94de5-121">Protocol specifications</span></span>

<span data-ttu-id="94de5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94de5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94de5-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="94de5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94de5-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94de5-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94de5-125">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний об объектах.</span><span class="sxs-lookup"><span data-stu-id="94de5-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94de5-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="94de5-126">Header files</span></span>

<span data-ttu-id="94de5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94de5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="94de5-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="94de5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94de5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="94de5-129">See also</span></span>



[<span data-ttu-id="94de5-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="94de5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94de5-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="94de5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94de5-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="94de5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94de5-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="94de5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

