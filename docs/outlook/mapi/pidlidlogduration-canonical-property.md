---
title: Каноническое свойство PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400344"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="2b44d-103">Каноническое свойство PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="2b44d-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="2b44d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b44d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b44d-105">Представляет интервал в минутах сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="2b44d-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b44d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2b44d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b44d-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="2b44d-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="2b44d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2b44d-108">Property set:</span></span>  <br/> |<span data-ttu-id="2b44d-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="2b44d-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="2b44d-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2b44d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2b44d-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="2b44d-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="2b44d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2b44d-112">Data type:</span></span>  <br/> |<span data-ttu-id="2b44d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b44d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b44d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2b44d-114">Area:</span></span>  <br/> |<span data-ttu-id="2b44d-115">������</span><span class="sxs-lookup"><span data-stu-id="2b44d-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b44d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b44d-116">Remarks</span></span>

<span data-ttu-id="2b44d-117">Интервал в минутах, действия, которые должны быть различие между свойствами **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) и **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2b44d-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b44d-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b44d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b44d-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2b44d-119">Protocol specifications</span></span>

<span data-ttu-id="2b44d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b44d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b44d-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2b44d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b44d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b44d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b44d-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="2b44d-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b44d-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2b44d-124">Header files</span></span>

<span data-ttu-id="2b44d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b44d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b44d-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2b44d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b44d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2b44d-127">See also</span></span>



[<span data-ttu-id="2b44d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b44d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b44d-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b44d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b44d-130">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="2b44d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b44d-131">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="2b44d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

