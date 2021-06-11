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
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="7e870-103">Каноническое свойство PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="7e870-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="7e870-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e870-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e870-105">Содержит TRUE, если отправитель сообщения хочет получить ответ на запрос собрания.</span><span class="sxs-lookup"><span data-stu-id="7e870-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e870-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7e870-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e870-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="7e870-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="7e870-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7e870-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e870-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="7e870-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="7e870-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7e870-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e870-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7e870-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7e870-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7e870-112">Area:</span></span>  <br/> |<span data-ttu-id="7e870-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="7e870-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e870-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e870-114">Remarks</span></span>

<span data-ttu-id="7e870-115">Это свойство используется для запросов на собрания.</span><span class="sxs-lookup"><span data-stu-id="7e870-115">This property is used for meeting requests.</span></span> <span data-ttu-id="7e870-116">Получающие клиентские приложения должны побудить пользователя принять или отклоть запрос, а затем отправить этот ответ обратно отправителю.</span><span class="sxs-lookup"><span data-stu-id="7e870-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e870-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e870-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e870-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7e870-118">Protocol specifications</span></span>

<span data-ttu-id="7e870-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e870-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e870-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="7e870-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e870-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e870-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e870-122">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7e870-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="7e870-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e870-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e870-124">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="7e870-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="7e870-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e870-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e870-126">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7e870-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e870-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="7e870-127">Header files</span></span>

<span data-ttu-id="7e870-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e870-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e870-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7e870-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e870-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7e870-130">Mapitags.h</span></span>
  
> <span data-ttu-id="7e870-131">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7e870-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e870-132">См. также</span><span class="sxs-lookup"><span data-stu-id="7e870-132">See also</span></span>



[<span data-ttu-id="7e870-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e870-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e870-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e870-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e870-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7e870-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e870-136">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="7e870-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

