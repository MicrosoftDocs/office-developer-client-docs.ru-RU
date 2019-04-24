---
title: Каноническое свойство PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336927"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="d619b-103">Каноническое свойство PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="d619b-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="d619b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d619b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d619b-105">Представляет дату и время окончания сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="d619b-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d619b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d619b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d619b-107">Диспидложенд</span><span class="sxs-lookup"><span data-stu-id="d619b-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="d619b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d619b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d619b-109">Псетид_лог</span><span class="sxs-lookup"><span data-stu-id="d619b-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="d619b-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d619b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d619b-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="d619b-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="d619b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d619b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d619b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d619b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d619b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d619b-114">Area:</span></span>  <br/> |<span data-ttu-id="d619b-115">Журнал</span><span class="sxs-lookup"><span data-stu-id="d619b-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d619b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d619b-116">Remarks</span></span>

<span data-ttu-id="d619b-117">Время окончания действия в формате UTC (UTC), которое должно совпадать со свойством **диспидкоммоненд** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) и большим или равным значению свойства **диспидлогстарт** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d619b-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d619b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d619b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d619b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d619b-119">Protocol specifications</span></span>

<span data-ttu-id="d619b-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d619b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d619b-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d619b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d619b-122">[[MS — ОКСОЖРНЛ]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d619b-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d619b-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="d619b-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d619b-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d619b-124">Header files</span></span>

<span data-ttu-id="d619b-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d619b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d619b-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d619b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d619b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d619b-127">See also</span></span>



[<span data-ttu-id="d619b-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d619b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d619b-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d619b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d619b-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d619b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d619b-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d619b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

