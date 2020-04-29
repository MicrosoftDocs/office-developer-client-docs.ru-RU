---
title: Каноническое свойство PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341050"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="b5cc0-103">Каноническое свойство PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="b5cc0-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="b5cc0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5cc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5cc0-105">Содержит исходные Дата и время отправки сообщения в отчете.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5cc0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b5cc0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5cc0-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="b5cc0-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="b5cc0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b5cc0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5cc0-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="b5cc0-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="b5cc0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b5cc0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5cc0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b5cc0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b5cc0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b5cc0-112">Area:</span></span>  <br/> |<span data-ttu-id="b5cc0-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="b5cc0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5cc0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5cc0-114">Remarks</span></span>

<span data-ttu-id="b5cc0-115">При первой отправке сообщения клиентскому приложению следует задать для этого свойства значение свойства **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b5cc0-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="b5cc0-116">При пересылке сообщения он не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="b5cc0-117">Используется только в отчетах.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5cc0-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5cc0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5cc0-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b5cc0-119">Protocol specifications</span></span>

<span data-ttu-id="b5cc0-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5cc0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5cc0-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5cc0-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5cc0-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5cc0-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5cc0-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b5cc0-124">Header files</span></span>

<span data-ttu-id="b5cc0-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b5cc0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5cc0-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5cc0-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b5cc0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b5cc0-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5cc0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b5cc0-129">See also</span></span>



[<span data-ttu-id="b5cc0-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cc0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5cc0-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cc0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5cc0-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cc0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5cc0-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b5cc0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

