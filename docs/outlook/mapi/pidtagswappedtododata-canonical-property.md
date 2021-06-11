---
title: Каноническое свойство PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359138"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="0309a-103">Каноническое свойство PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="0309a-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="0309a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0309a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0309a-105">Поддерживает второй набор значений свойств, которые не влияют на состояние помеченного объекта Message.</span><span class="sxs-lookup"><span data-stu-id="0309a-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0309a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0309a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0309a-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="0309a-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="0309a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0309a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0309a-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="0309a-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="0309a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0309a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0309a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0309a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0309a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0309a-112">Area:</span></span>  <br/> |<span data-ttu-id="0309a-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="0309a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0309a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0309a-114">Remarks</span></span>

<span data-ttu-id="0309a-115">Действуя в качестве дополнительного расположения хранилища флагов, если поддерживаются флаги отправитель или напоминания отправитель, эта структура предоставляет расположение, в котором хранятся все свойства, относящиеся к протоколу информационного флажка, поддерживаемые в флагах отправитель, и все свойства, связанные с протоколом напоминания Параметры, которые поддерживаются в напоминаниях отправитель, не подвергая получателям сообщения флаг отправитель или отправитель напоминания.</span><span class="sxs-lookup"><span data-stu-id="0309a-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="0309a-116">Кроме того, эта структура предоставляет расположение, в котором хранятся все свойства, относящиеся к протоколу информационной маркировки, поддерживаемые в флагах получателей и свойствах, связанных с протоколом reminder Параметры, которые поддерживаются в напоминаниях получателей в ранее отправленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="0309a-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="0309a-117">Дополнительные сведения об этом свойстве [см. в [MS-OXOFLAG].](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0309a-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0309a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0309a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0309a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0309a-119">Protocol specifications</span></span>

<span data-ttu-id="0309a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0309a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0309a-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0309a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0309a-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0309a-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0309a-123">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="0309a-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="0309a-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0309a-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0309a-125">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.</span><span class="sxs-lookup"><span data-stu-id="0309a-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0309a-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0309a-126">Header files</span></span>

<span data-ttu-id="0309a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0309a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0309a-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0309a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0309a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0309a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0309a-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0309a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0309a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0309a-131">See also</span></span>



[<span data-ttu-id="0309a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0309a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0309a-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0309a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0309a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0309a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0309a-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0309a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

