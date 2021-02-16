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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421566"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="ba4bb-103">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="ba4bb-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="ba4bb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba4bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba4bb-105">Содержит сообщение, которое указывает текущее состояние ресурса сеанса.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba4bb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ba4bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba4bb-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="ba4bb-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="ba4bb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ba4bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba4bb-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="ba4bb-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="ba4bb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ba4bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba4bb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ba4bb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ba4bb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ba4bb-112">Area:</span></span>  <br/> |<span data-ttu-id="ba4bb-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba4bb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba4bb-114">Remarks</span></span>

<span data-ttu-id="ba4bb-115">Эти свойства дают поставщикам услуг и MAPI возможность предоставить определенные сведения о состоянии ресурса сеанса, например интегрированную адресную книгу или конкретного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="ba4bb-116">Это свойство поясняет и предоставляет дополнительные сведения о коде состояния или свойстве **PR_STATUS_CODE** ([PidTagStatusCode).](pidtagstatuscode-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ba4bb-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="ba4bb-117">В то **PR_STATUS_CODE** требуется для всех объектов **состояния,** PR_STATUS_STRING и связанные свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="ba4bb-118">Если поставщик транспорта не укавит значение, то для пула MAPI будет запулярно значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="ba4bb-119">Строка создается на той же стороне удаленного вызова процедуры, что и пулер MAPI; он проходит через общую память, а не маршалуется через границу процесса.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba4bb-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ba4bb-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba4bb-121">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ba4bb-121">Header files</span></span>

<span data-ttu-id="ba4bb-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba4bb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba4bb-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba4bb-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba4bb-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ba4bb-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ba4bb-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba4bb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ba4bb-126">See also</span></span>



[<span data-ttu-id="ba4bb-127">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="ba4bb-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="ba4bb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba4bb-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba4bb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ba4bb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba4bb-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ba4bb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

