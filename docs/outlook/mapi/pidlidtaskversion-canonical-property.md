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
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="6c8dd-103">Каноническое свойство PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="6c8dd-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="6c8dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c8dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c8dd-105">Указывает, какая копия является последним обновлением задачи.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c8dd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6c8dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c8dd-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="6c8dd-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="6c8dd-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6c8dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c8dd-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6c8dd-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6c8dd-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="6c8dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c8dd-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="6c8dd-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="6c8dd-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6c8dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c8dd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c8dd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c8dd-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6c8dd-114">Area:</span></span>  <br/> |<span data-ttu-id="6c8dd-115">Task</span><span class="sxs-lookup"><span data-stu-id="6c8dd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c8dd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c8dd-116">Remarks</span></span>

<span data-ttu-id="6c8dd-117">Обновления с более низкими версиями, чем задача, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="6c8dd-118">При внедрении задачи в связь с задачей клиент также задает текущую версию внедренной задачи для связи с задачей.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c8dd-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6c8dd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c8dd-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6c8dd-120">Protocol specifications</span></span>

<span data-ttu-id="6c8dd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c8dd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c8dd-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c8dd-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c8dd-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c8dd-124">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c8dd-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6c8dd-125">Header files</span></span>

<span data-ttu-id="6c8dd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c8dd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c8dd-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6c8dd-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c8dd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6c8dd-128">See also</span></span>



[<span data-ttu-id="6c8dd-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6c8dd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c8dd-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6c8dd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c8dd-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6c8dd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c8dd-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6c8dd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

