---
title: Каноническое свойство PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385839"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="143f0-103">Каноническое свойство PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="143f0-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="143f0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="143f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="143f0-105">Содержит дату и время отправки сообщения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="143f0-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="143f0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="143f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="143f0-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="143f0-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="143f0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="143f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="143f0-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="143f0-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="143f0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="143f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="143f0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="143f0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="143f0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="143f0-112">Area:</span></span>  <br/> |<span data-ttu-id="143f0-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="143f0-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="143f0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="143f0-114">Remarks</span></span>

<span data-ttu-id="143f0-115">Поставщик хранения задается **PR_CLIENT_SUBMIT_TIME** времени, который клиентское приложение вызывать [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="143f0-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="143f0-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="143f0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="143f0-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="143f0-117">Protocol specifications</span></span>

<span data-ttu-id="143f0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="143f0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="143f0-119">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="143f0-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="143f0-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="143f0-120">Header files</span></span>

<span data-ttu-id="143f0-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="143f0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="143f0-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="143f0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="143f0-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="143f0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="143f0-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="143f0-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="143f0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="143f0-125">See also</span></span>



[<span data-ttu-id="143f0-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="143f0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="143f0-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="143f0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="143f0-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="143f0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="143f0-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="143f0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

