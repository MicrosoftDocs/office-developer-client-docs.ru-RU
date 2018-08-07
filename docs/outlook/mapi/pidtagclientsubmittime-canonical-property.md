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
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810918"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="72a57-103">Каноническое свойство PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="72a57-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="72a57-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72a57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72a57-105">Содержит дату и время отправки сообщения отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="72a57-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72a57-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="72a57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72a57-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="72a57-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="72a57-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="72a57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72a57-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="72a57-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="72a57-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="72a57-110">Data type:</span></span>  <br/> |<span data-ttu-id="72a57-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="72a57-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="72a57-112">Область:</span><span class="sxs-lookup"><span data-stu-id="72a57-112">Area:</span></span>  <br/> |<span data-ttu-id="72a57-113">Время сообщения</span><span class="sxs-lookup"><span data-stu-id="72a57-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72a57-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="72a57-114">Remarks</span></span>

<span data-ttu-id="72a57-115">Поставщик хранения задается **PR_CLIENT_SUBMIT_TIME** времени, который клиентское приложение вызывать [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="72a57-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72a57-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72a57-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72a57-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="72a57-117">Protocol specifications</span></span>

<span data-ttu-id="72a57-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72a57-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72a57-119">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="72a57-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72a57-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="72a57-120">Header files</span></span>

<span data-ttu-id="72a57-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72a57-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="72a57-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="72a57-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="72a57-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72a57-123">Mapitags.h</span></span>
  
> <span data-ttu-id="72a57-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="72a57-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72a57-125">См. также</span><span class="sxs-lookup"><span data-stu-id="72a57-125">See also</span></span>



[<span data-ttu-id="72a57-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72a57-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72a57-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72a57-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72a57-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="72a57-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72a57-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="72a57-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

