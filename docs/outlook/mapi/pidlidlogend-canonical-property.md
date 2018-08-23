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
ms.openlocfilehash: 739fe4077fa57f0f12dd38f05f90851c5291b45a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585936"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="7a6c0-103">Каноническое свойство PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="7a6c0-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="7a6c0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a6c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a6c0-105">Представляет Дата и время окончания для сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="7a6c0-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a6c0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7a6c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a6c0-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="7a6c0-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="7a6c0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7a6c0-108">Property set:</span></span>  <br/> |<span data-ttu-id="7a6c0-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="7a6c0-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="7a6c0-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7a6c0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7a6c0-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="7a6c0-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="7a6c0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7a6c0-112">Data type:</span></span>  <br/> |<span data-ttu-id="7a6c0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7a6c0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7a6c0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="7a6c0-114">Area:</span></span>  <br/> |<span data-ttu-id="7a6c0-115">������</span><span class="sxs-lookup"><span data-stu-id="7a6c0-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a6c0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a6c0-116">Remarks</span></span>

<span data-ttu-id="7a6c0-117">Время действия завершения в формате UTC (UTC), которое должно быть равно свойству **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) и больше или равно свойству **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7a6c0-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a6c0-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7a6c0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a6c0-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7a6c0-119">Protocol specifications</span></span>

<span data-ttu-id="7a6c0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a6c0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a6c0-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7a6c0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a6c0-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a6c0-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a6c0-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="7a6c0-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a6c0-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7a6c0-124">Header files</span></span>

<span data-ttu-id="7a6c0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a6c0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a6c0-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7a6c0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a6c0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7a6c0-127">See also</span></span>



[<span data-ttu-id="7a6c0-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a6c0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a6c0-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7a6c0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a6c0-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7a6c0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a6c0-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7a6c0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

