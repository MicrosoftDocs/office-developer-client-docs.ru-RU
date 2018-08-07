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
ms.openlocfilehash: f4675362de1e9efe4ef16285723cddeface9c403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810468"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="63719-103">Каноническое свойство PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="63719-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="63719-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63719-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63719-105">Указывает, что внесенные пользователя о ходе выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="63719-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63719-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63719-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63719-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="63719-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="63719-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="63719-108">Property set:</span></span>  <br/> |<span data-ttu-id="63719-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="63719-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="63719-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="63719-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63719-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="63719-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="63719-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63719-112">Data type:</span></span>  <br/> |<span data-ttu-id="63719-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="63719-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="63719-114">Область:</span><span class="sxs-lookup"><span data-stu-id="63719-114">Area:</span></span>  <br/> |<span data-ttu-id="63719-115">Task</span><span class="sxs-lookup"><span data-stu-id="63719-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63719-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="63719-116">Remarks</span></span>

<span data-ttu-id="63719-117">Значение этого свойства должно быть число, большее или равное 0,0 и меньше, чем или равно 1.0, где 1.0 указывает, что завершено и 0,0 указывает, что не начала работы.</span><span class="sxs-lookup"><span data-stu-id="63719-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="63719-118">Для объекта message отметкой времени значение этого свойства необходимо установить значение 1.0 Если объект помечен завершенных и необходимо указать в противном случае — значение 0.0.</span><span class="sxs-lookup"><span data-stu-id="63719-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63719-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63719-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63719-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="63719-120">Protocol specifications</span></span>

<span data-ttu-id="63719-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="63719-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63719-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="63719-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="63719-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-126">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="63719-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="63719-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-128">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="63719-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="63719-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-130">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="63719-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="63719-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63719-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63719-132">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="63719-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63719-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="63719-133">Header files</span></span>

<span data-ttu-id="63719-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63719-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="63719-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63719-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63719-136">См. также</span><span class="sxs-lookup"><span data-stu-id="63719-136">See also</span></span>



[<span data-ttu-id="63719-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63719-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63719-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63719-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63719-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63719-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63719-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="63719-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

