---
title: Каноническое свойство PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387183"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="82722-103">Каноническое свойство PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="82722-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="82722-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82722-105">Указывает, что задача была создана с помощью текущего пользователя или агент пользователя, а не при обработке запроса на задачу.</span><span class="sxs-lookup"><span data-stu-id="82722-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82722-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="82722-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82722-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="82722-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="82722-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="82722-108">Property set:</span></span>  <br/> |<span data-ttu-id="82722-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="82722-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="82722-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="82722-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="82722-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="82722-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="82722-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="82722-112">Data type:</span></span>  <br/> |<span data-ttu-id="82722-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="82722-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="82722-114">Область:</span><span class="sxs-lookup"><span data-stu-id="82722-114">Area:</span></span>  <br/> |<span data-ttu-id="82722-115">Task</span><span class="sxs-lookup"><span data-stu-id="82722-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82722-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="82722-116">Remarks</span></span>

<span data-ttu-id="82722-117">Клиент этому свойству значение TRUE, когда пользователь создает задачу и значение FALSE при назначении задачи другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="82722-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="82722-118">Если оставить это свойство определено, предполагается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="82722-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82722-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82722-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82722-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="82722-120">Protocol specifications</span></span>

<span data-ttu-id="82722-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82722-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82722-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="82722-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82722-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82722-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82722-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="82722-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82722-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="82722-125">Header files</span></span>

<span data-ttu-id="82722-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82722-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="82722-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="82722-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82722-128">См. также</span><span class="sxs-lookup"><span data-stu-id="82722-128">See also</span></span>



[<span data-ttu-id="82722-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82722-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82722-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82722-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82722-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="82722-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82722-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="82722-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

