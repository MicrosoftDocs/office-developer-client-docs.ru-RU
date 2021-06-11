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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303082"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="8ed02-103">Каноническое свойство PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="8ed02-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="8ed02-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ed02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ed02-105">Указывает, что задача изначально была создана текущим пользователем или агентом пользователя, а не обработкой запроса задачи.</span><span class="sxs-lookup"><span data-stu-id="8ed02-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed02-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ed02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ed02-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="8ed02-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="8ed02-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8ed02-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ed02-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="8ed02-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="8ed02-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8ed02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ed02-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="8ed02-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="8ed02-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ed02-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ed02-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8ed02-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8ed02-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8ed02-114">Area:</span></span>  <br/> |<span data-ttu-id="8ed02-115">Задача</span><span class="sxs-lookup"><span data-stu-id="8ed02-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed02-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed02-116">Remarks</span></span>

<span data-ttu-id="8ed02-117">Клиент задает это свойство TRUE, когда пользователь создает задачу, и FALSE, когда задача назначена другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="8ed02-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="8ed02-118">Если это свойство остается неустановленным, предполагается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8ed02-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8ed02-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ed02-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ed02-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ed02-120">Protocol specifications</span></span>

<span data-ttu-id="8ed02-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed02-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ed02-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8ed02-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ed02-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed02-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ed02-124">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="8ed02-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ed02-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8ed02-125">Header files</span></span>

<span data-ttu-id="8ed02-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ed02-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ed02-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ed02-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed02-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8ed02-128">See also</span></span>



[<span data-ttu-id="8ed02-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed02-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ed02-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed02-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ed02-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed02-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ed02-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8ed02-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

