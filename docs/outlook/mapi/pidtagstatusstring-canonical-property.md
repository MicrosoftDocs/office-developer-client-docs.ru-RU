---
title: Каноническое свойство PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e8370a613162e3bc8d4395a18e9a7e177255b9b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567302"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="5bfbf-103">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="5bfbf-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="5bfbf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bfbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bfbf-105">Содержит сообщение, указывающее текущее состояние сеанса ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bfbf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bfbf-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="5bfbf-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="5bfbf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bfbf-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="5bfbf-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="5bfbf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bfbf-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5bfbf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5bfbf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-112">Area:</span></span>  <br/> |<span data-ttu-id="5bfbf-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfbf-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bfbf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bfbf-114">Remarks</span></span>

<span data-ttu-id="5bfbf-115">Эти свойства предоставьте поставщиков услуг и MAPI возможность предоставить определенные сведения о состоянии сеанса ресурса, например интегрированной адресной книги или поставщик конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="5bfbf-116">Это свойство объясняется, а также предоставляются дополнительные сведения о код состояния или свойство **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5bfbf-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="5bfbf-117">В то время как **PR_STATUS_CODE** является обязательным для всех объектов состояния, **PR_STATUS_STRING** и связанные свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="5bfbf-118">Когда поставщика транспорта не задано значение, диспетчер очереди MAPI предоставляет значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="5bfbf-119">Строка создается в части удаленный вызов процедур, как диспетчер очереди MAPI; он проходит через общей памяти, а не выполняется упаковать через границы процессов.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bfbf-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bfbf-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5bfbf-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5bfbf-121">Header files</span></span>

<span data-ttu-id="5bfbf-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bfbf-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bfbf-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bfbf-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bfbf-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5bfbf-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bfbf-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5bfbf-126">See also</span></span>



[<span data-ttu-id="5bfbf-127">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="5bfbf-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="5bfbf-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfbf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bfbf-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfbf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bfbf-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfbf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bfbf-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5bfbf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

