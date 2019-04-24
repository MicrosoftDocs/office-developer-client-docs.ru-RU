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
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278895"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="7f73c-103">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="7f73c-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="7f73c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f73c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f73c-105">Содержит сообщение с указанием текущего состояния ресурса сеанса.</span><span class="sxs-lookup"><span data-stu-id="7f73c-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f73c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7f73c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f73c-107">ПР_СТАТУС_СТРИНГ, ПР_СТАТУС_СТРИНГ_А, ПР_СТАТУС_СТРИНГ_В</span><span class="sxs-lookup"><span data-stu-id="7f73c-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="7f73c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7f73c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f73c-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="7f73c-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="7f73c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7f73c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f73c-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="7f73c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7f73c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7f73c-112">Area:</span></span>  <br/> |<span data-ttu-id="7f73c-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="7f73c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f73c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7f73c-114">Remarks</span></span>

<span data-ttu-id="7f73c-115">Эти свойства предоставляют поставщикам услуг и MAPI возможность предоставлять конкретные сведения о состоянии ресурса сеанса, например интегрированной адресной книге или определенном поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="7f73c-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="7f73c-116">Это свойство объясняет и предоставляет дополнительные сведения о коде состояния или свойстве **пр_статус_коде** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f73c-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="7f73c-117">В то время как **пр_статус_коде** является обязательным для всех объектов status, **пр_статус_стринг** и связанные свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="7f73c-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="7f73c-118">Когда поставщик транспорта не предоставляет значение, диспетчер очереди MAPI предоставляет значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f73c-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="7f73c-119">Строка создается на той же стороне удаленного вызова процедуры, что и Диспетчер очереди MAPI; он перемещается через общую память, а не упаковывается в пределах границы процесса.</span><span class="sxs-lookup"><span data-stu-id="7f73c-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f73c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7f73c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f73c-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="7f73c-121">Header files</span></span>

<span data-ttu-id="7f73c-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7f73c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f73c-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7f73c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f73c-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7f73c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7f73c-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="7f73c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f73c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7f73c-126">See also</span></span>



[<span data-ttu-id="7f73c-127">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="7f73c-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="7f73c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7f73c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f73c-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7f73c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f73c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7f73c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f73c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7f73c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

