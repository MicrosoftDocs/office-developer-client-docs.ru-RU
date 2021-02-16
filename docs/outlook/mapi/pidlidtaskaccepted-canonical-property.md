---
title: Каноническое свойство PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331285"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="f23f0-103">Каноническое свойство PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="f23f0-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="f23f0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f23f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f23f0-105">Указывает, ответил ли назначаемая задача на запрос задачи.</span><span class="sxs-lookup"><span data-stu-id="f23f0-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f23f0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f23f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f23f0-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="f23f0-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="f23f0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f23f0-108">Property set:</span></span>  <br/> |<span data-ttu-id="f23f0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f23f0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f23f0-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f23f0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f23f0-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="f23f0-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="f23f0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f23f0-112">Data type:</span></span>  <br/> |<span data-ttu-id="f23f0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f23f0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f23f0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f23f0-114">Area:</span></span>  <br/> |<span data-ttu-id="f23f0-115">Task</span><span class="sxs-lookup"><span data-stu-id="f23f0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f23f0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f23f0-116">Remarks</span></span>

<span data-ttu-id="f23f0-117">Клиент устанавливает для этого свойства false для новой задачи или устанавливает для этого свойства true, когда задача принимается или отклоняется.</span><span class="sxs-lookup"><span data-stu-id="f23f0-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="f23f0-118">Если свойство не замечено, предполагается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="f23f0-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f23f0-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f23f0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f23f0-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f23f0-120">Protocol specifications</span></span>

<span data-ttu-id="f23f0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f23f0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f23f0-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="f23f0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f23f0-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f23f0-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f23f0-124">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f23f0-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f23f0-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f23f0-125">Header files</span></span>

<span data-ttu-id="f23f0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f23f0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f23f0-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f23f0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f23f0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f23f0-128">See also</span></span>



[<span data-ttu-id="f23f0-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f23f0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f23f0-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f23f0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f23f0-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f23f0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f23f0-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f23f0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

