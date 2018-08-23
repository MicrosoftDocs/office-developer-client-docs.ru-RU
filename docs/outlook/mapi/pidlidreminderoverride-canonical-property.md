---
title: Каноническое свойство PidLidReminderOverride
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55aa8e47dda82995ca1d246f36c271ef06e66954
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580182"
---
# <a name="pidlidreminderoverride-canonical-property"></a><span data-ttu-id="05161-103">Каноническое свойство PidLidReminderOverride</span><span class="sxs-lookup"><span data-stu-id="05161-103">PidLidReminderOverride Canonical Property</span></span>

  
  
<span data-ttu-id="05161-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05161-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05161-105">Указывает, будет ли клиента должны учитывать значения свойства **dispidReminderFileParam** ( [PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) и **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="05161-105">Specifies whether the client should respect the values of the **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) and **dispidReminderFileParam** ( [ PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) properties.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05161-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="05161-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05161-107">dispidReminderOverride</span><span class="sxs-lookup"><span data-stu-id="05161-107">dispidReminderOverride</span></span>  <br/> |
|<span data-ttu-id="05161-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="05161-108">Property set:</span></span>  <br/> |<span data-ttu-id="05161-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="05161-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="05161-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="05161-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05161-111">0x0000851C</span><span class="sxs-lookup"><span data-stu-id="05161-111">0x0000851C</span></span>  <br/> |
|<span data-ttu-id="05161-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="05161-112">Data type:</span></span>  <br/> |<span data-ttu-id="05161-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="05161-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="05161-114">Область:</span><span class="sxs-lookup"><span data-stu-id="05161-114">Area:</span></span>  <br/> |<span data-ttu-id="05161-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="05161-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05161-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="05161-116">Remarks</span></span>

<span data-ttu-id="05161-117">Клиент может использовать значения по умолчанию вместо значений свойств **dispidReminderPlaySound** и **dispidReminderFileParam** .</span><span class="sxs-lookup"><span data-stu-id="05161-117">A client may use default values in place of the values of the **dispidReminderPlaySound** and **dispidReminderFileParam** properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="05161-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="05161-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05161-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="05161-119">Protocol specifications</span></span>

<span data-ttu-id="05161-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05161-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05161-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="05161-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05161-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05161-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05161-123">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="05161-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05161-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="05161-124">Header files</span></span>

<span data-ttu-id="05161-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05161-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="05161-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="05161-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05161-127">См. также</span><span class="sxs-lookup"><span data-stu-id="05161-127">See also</span></span>



[<span data-ttu-id="05161-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="05161-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05161-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="05161-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05161-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="05161-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05161-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="05161-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

