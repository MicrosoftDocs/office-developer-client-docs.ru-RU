---
title: Каноническое свойство PidTagResponseRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330158"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="1c67e-103">Каноническое свойство PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="1c67e-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="1c67e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c67e-105">Содержит значение TRUE, если отправителю требуется ответ на приглашение на собрание.</span><span class="sxs-lookup"><span data-stu-id="1c67e-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c67e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1c67e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c67e-107">ПР_РЕСПОНСЕ_РЕКУЕСТЕД</span><span class="sxs-lookup"><span data-stu-id="1c67e-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="1c67e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1c67e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c67e-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="1c67e-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="1c67e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1c67e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c67e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1c67e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1c67e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1c67e-112">Area:</span></span>  <br/> |<span data-ttu-id="1c67e-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="1c67e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c67e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c67e-114">Remarks</span></span>

<span data-ttu-id="1c67e-115">Это свойство используется для приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="1c67e-115">This property is used for meeting requests.</span></span> <span data-ttu-id="1c67e-116">Принимающее клиентское приложение должно предложить пользователю принять или отклонить запрос, а затем отправить ответ отправителю.</span><span class="sxs-lookup"><span data-stu-id="1c67e-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c67e-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1c67e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c67e-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1c67e-118">Protocol specifications</span></span>

<span data-ttu-id="1c67e-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c67e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c67e-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1c67e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c67e-121">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c67e-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c67e-122">Задает свойства и операции, допустимые для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1c67e-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="1c67e-123">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c67e-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c67e-124">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="1c67e-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="1c67e-125">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c67e-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c67e-126">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1c67e-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c67e-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="1c67e-127">Header files</span></span>

<span data-ttu-id="1c67e-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1c67e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c67e-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1c67e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c67e-130">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="1c67e-130">Mapitags.h</span></span>
  
> <span data-ttu-id="1c67e-131">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="1c67e-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c67e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1c67e-132">See also</span></span>



[<span data-ttu-id="1c67e-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1c67e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c67e-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="1c67e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c67e-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1c67e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c67e-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1c67e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

