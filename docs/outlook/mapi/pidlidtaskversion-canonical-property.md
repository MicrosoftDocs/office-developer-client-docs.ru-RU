---
title: Каноническое свойство PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356495"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="b700d-103">Каноническое свойство PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="b700d-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="b700d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b700d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b700d-105">Указывает, какая копия является последним обновлением задачи.</span><span class="sxs-lookup"><span data-stu-id="b700d-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b700d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b700d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b700d-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="b700d-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="b700d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b700d-108">Property set:</span></span>  <br/> |<span data-ttu-id="b700d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b700d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b700d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b700d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b700d-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="b700d-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="b700d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b700d-112">Data type:</span></span>  <br/> |<span data-ttu-id="b700d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b700d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b700d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b700d-114">Area:</span></span>  <br/> |<span data-ttu-id="b700d-115">Задача</span><span class="sxs-lookup"><span data-stu-id="b700d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b700d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b700d-116">Remarks</span></span>

<span data-ttu-id="b700d-117">Обновления с более низкими версиями, чем задача, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b700d-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="b700d-118">При вложении задачи в сообщение задачи клиент задает текущую версию встроенной задачи и в связи с задачами.</span><span class="sxs-lookup"><span data-stu-id="b700d-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b700d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b700d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b700d-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b700d-120">Protocol specifications</span></span>

<span data-ttu-id="b700d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b700d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b700d-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b700d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b700d-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b700d-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b700d-124">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="b700d-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b700d-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b700d-125">Header files</span></span>

<span data-ttu-id="b700d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b700d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b700d-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b700d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b700d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b700d-128">See also</span></span>



[<span data-ttu-id="b700d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b700d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b700d-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b700d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b700d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b700d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b700d-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b700d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

