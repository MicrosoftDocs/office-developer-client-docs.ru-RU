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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386042"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="a644a-103">Каноническое свойство PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="a644a-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="a644a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a644a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a644a-105">Указывает, какие копию последнего обновления задачи.</span><span class="sxs-lookup"><span data-stu-id="a644a-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a644a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a644a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a644a-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="a644a-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="a644a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a644a-108">Property set:</span></span>  <br/> |<span data-ttu-id="a644a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a644a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a644a-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a644a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a644a-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="a644a-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="a644a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a644a-112">Data type:</span></span>  <br/> |<span data-ttu-id="a644a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a644a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a644a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a644a-114">Area:</span></span>  <br/> |<span data-ttu-id="a644a-115">Task</span><span class="sxs-lookup"><span data-stu-id="a644a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a644a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a644a-116">Remarks</span></span>

<span data-ttu-id="a644a-117">Обновление с версии меньше, чем игнорируются.</span><span class="sxs-lookup"><span data-stu-id="a644a-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="a644a-118">При внедрении задачи в связи задач, клиент задает текущую версию внедренных задач также связи задач.</span><span class="sxs-lookup"><span data-stu-id="a644a-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a644a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a644a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a644a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a644a-120">Protocol specifications</span></span>

<span data-ttu-id="a644a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a644a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a644a-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a644a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a644a-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a644a-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a644a-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="a644a-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a644a-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a644a-125">Header files</span></span>

<span data-ttu-id="a644a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a644a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a644a-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a644a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a644a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a644a-128">See also</span></span>



[<span data-ttu-id="a644a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a644a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a644a-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a644a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a644a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a644a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a644a-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a644a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

