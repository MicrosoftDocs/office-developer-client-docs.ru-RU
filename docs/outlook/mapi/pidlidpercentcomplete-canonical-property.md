---
title: Каноническое свойство PidLidPercentComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357976"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="763cd-103">Каноническое свойство PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="763cd-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="763cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="763cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="763cd-105">Показывает ход выполнения задачи пользователем.</span><span class="sxs-lookup"><span data-stu-id="763cd-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="763cd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="763cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="763cd-107">Диспидперценткомплете</span><span class="sxs-lookup"><span data-stu-id="763cd-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="763cd-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="763cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="763cd-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="763cd-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="763cd-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="763cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="763cd-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="763cd-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="763cd-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="763cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="763cd-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="763cd-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="763cd-114">Область:</span><span class="sxs-lookup"><span data-stu-id="763cd-114">Area:</span></span>  <br/> |<span data-ttu-id="763cd-115">Задача</span><span class="sxs-lookup"><span data-stu-id="763cd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="763cd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="763cd-116">Remarks</span></span>

<span data-ttu-id="763cd-117">Значение этого свойства должно быть числом, превышающим или равным 0,0 и меньшим или равным 1,0, где 1,0 означает, что работа завершена, а 0,0 означает, что работа еще не началась.</span><span class="sxs-lookup"><span data-stu-id="763cd-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="763cd-118">Для объекта Message с отметкой времени значение этого свойства должно быть равно 1,0, если объект помечен как завершенный, и для него должно быть задано значение 0,0 в ином случае.</span><span class="sxs-lookup"><span data-stu-id="763cd-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="763cd-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="763cd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="763cd-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="763cd-120">Protocol specifications</span></span>

<span data-ttu-id="763cd-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="763cd-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="763cd-123">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-124">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="763cd-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="763cd-125">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-126">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="763cd-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="763cd-127">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-128">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="763cd-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="763cd-129">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-130">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="763cd-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="763cd-131">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="763cd-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="763cd-132">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="763cd-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="763cd-133">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="763cd-133">Header files</span></span>

<span data-ttu-id="763cd-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="763cd-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="763cd-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="763cd-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="763cd-136">См. также</span><span class="sxs-lookup"><span data-stu-id="763cd-136">See also</span></span>



[<span data-ttu-id="763cd-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="763cd-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="763cd-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="763cd-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="763cd-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="763cd-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="763cd-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="763cd-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

