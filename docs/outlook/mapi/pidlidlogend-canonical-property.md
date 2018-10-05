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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398943"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="8c29b-103">Каноническое свойство PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="8c29b-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="8c29b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c29b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c29b-105">Представляет Дата и время окончания для сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="8c29b-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c29b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8c29b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c29b-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="8c29b-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="8c29b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8c29b-108">Property set:</span></span>  <br/> |<span data-ttu-id="8c29b-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="8c29b-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="8c29b-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8c29b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8c29b-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="8c29b-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="8c29b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8c29b-112">Data type:</span></span>  <br/> |<span data-ttu-id="8c29b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8c29b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8c29b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8c29b-114">Area:</span></span>  <br/> |<span data-ttu-id="8c29b-115">������</span><span class="sxs-lookup"><span data-stu-id="8c29b-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c29b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c29b-116">Remarks</span></span>

<span data-ttu-id="8c29b-117">Время действия завершения в формате UTC (UTC), которое должно быть равно свойству **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) и больше или равно свойству **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8c29b-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c29b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c29b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c29b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8c29b-119">Protocol specifications</span></span>

<span data-ttu-id="8c29b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c29b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c29b-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8c29b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c29b-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c29b-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c29b-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="8c29b-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c29b-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8c29b-124">Header files</span></span>

<span data-ttu-id="8c29b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c29b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c29b-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8c29b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c29b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8c29b-127">See also</span></span>



[<span data-ttu-id="8c29b-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c29b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c29b-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c29b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c29b-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8c29b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c29b-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8c29b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

