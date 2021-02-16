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
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350857"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="56d24-103">Каноническое свойство PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="56d24-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="56d24-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56d24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56d24-105">Указывает точку во времени, когда напоминание переходит из ожидающих сообщений в просроченные.</span><span class="sxs-lookup"><span data-stu-id="56d24-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56d24-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="56d24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56d24-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="56d24-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="56d24-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="56d24-108">Property set:</span></span>  <br/> |<span data-ttu-id="56d24-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="56d24-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="56d24-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="56d24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56d24-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="56d24-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="56d24-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="56d24-112">Data type:</span></span>  <br/> |<span data-ttu-id="56d24-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="56d24-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="56d24-114">Область:</span><span class="sxs-lookup"><span data-stu-id="56d24-114">Area:</span></span>  <br/> |<span data-ttu-id="56d24-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="56d24-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56d24-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="56d24-116">Remarks</span></span>

<span data-ttu-id="56d24-117">Это свойство должно быть установлено, если свойство **dispidReminderSet** ([PidLidReminderSet)](pidlidreminderset-canonical-property.md)имеет true.</span><span class="sxs-lookup"><span data-stu-id="56d24-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="56d24-118">Клиенты должны установить значение в UTC.</span><span class="sxs-lookup"><span data-stu-id="56d24-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56d24-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56d24-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56d24-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="56d24-120">Protocol specifications</span></span>

<span data-ttu-id="56d24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56d24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56d24-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="56d24-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56d24-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56d24-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56d24-124">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний об объектах.</span><span class="sxs-lookup"><span data-stu-id="56d24-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56d24-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="56d24-125">Header files</span></span>

<span data-ttu-id="56d24-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56d24-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="56d24-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="56d24-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56d24-128">См. также</span><span class="sxs-lookup"><span data-stu-id="56d24-128">See also</span></span>



[<span data-ttu-id="56d24-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56d24-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56d24-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56d24-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56d24-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="56d24-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56d24-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="56d24-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

