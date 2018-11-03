---
title: Каноническое свойство PidLidLogStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396269"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="62336-103">Каноническое свойство PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="62336-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="62336-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62336-105">Представляет дату и время начала для сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="62336-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62336-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="62336-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62336-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="62336-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="62336-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="62336-108">Property set:</span></span>  <br/> |<span data-ttu-id="62336-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="62336-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="62336-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="62336-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62336-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="62336-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="62336-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="62336-112">Data type:</span></span>  <br/> |<span data-ttu-id="62336-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="62336-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="62336-114">Область:</span><span class="sxs-lookup"><span data-stu-id="62336-114">Area:</span></span>  <br/> |<span data-ttu-id="62336-115">������</span><span class="sxs-lookup"><span data-stu-id="62336-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62336-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="62336-116">Remarks</span></span>

<span data-ttu-id="62336-117">Время в формате UTC (UTC) во время начала операции должно быть равно свойству **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62336-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62336-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62336-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62336-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="62336-119">Protocol specifications</span></span>

<span data-ttu-id="62336-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62336-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62336-121">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="62336-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62336-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62336-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62336-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="62336-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62336-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="62336-124">Header files</span></span>

<span data-ttu-id="62336-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62336-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="62336-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="62336-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62336-127">См. также</span><span class="sxs-lookup"><span data-stu-id="62336-127">See also</span></span>



[<span data-ttu-id="62336-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62336-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62336-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62336-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62336-130">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="62336-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62336-131">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="62336-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

