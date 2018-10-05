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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396745"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="2e275-103">Каноническое свойство PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="2e275-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="2e275-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e275-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e275-105">Содержит значение TRUE, если отправитель сообщения запрашивает ответ на приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="2e275-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e275-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2e275-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e275-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="2e275-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="2e275-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2e275-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e275-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="2e275-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="2e275-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2e275-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e275-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2e275-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2e275-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2e275-112">Area:</span></span>  <br/> |<span data-ttu-id="2e275-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="2e275-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e275-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2e275-114">Remarks</span></span>

<span data-ttu-id="2e275-115">Это свойство используется для приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="2e275-115">This property is used for meeting requests.</span></span> <span data-ttu-id="2e275-116">Получение клиентского приложения должен предложить пользователю принять или отклонить приглашение, а затем отправьте этот ответа отправителю.</span><span class="sxs-lookup"><span data-stu-id="2e275-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e275-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e275-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e275-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2e275-118">Protocol specifications</span></span>

<span data-ttu-id="2e275-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e275-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e275-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2e275-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e275-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e275-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e275-122">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2e275-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="2e275-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e275-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e275-124">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="2e275-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="2e275-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e275-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e275-126">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="2e275-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e275-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2e275-127">Header files</span></span>

<span data-ttu-id="2e275-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e275-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e275-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2e275-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e275-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e275-130">Mapitags.h</span></span>
  
> <span data-ttu-id="2e275-131">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2e275-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e275-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2e275-132">See also</span></span>



[<span data-ttu-id="2e275-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e275-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e275-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e275-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e275-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2e275-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e275-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2e275-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

