---
title: Каноническое свойство PidTagReportTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 95972d53f20f432bc8007f8bbc6734889773f938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811728"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="a9db7-103">Каноническое свойство PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="a9db7-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="a9db7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9db7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9db7-105">Содержит дату и время создания отчета в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a9db7-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9db7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a9db7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9db7-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="a9db7-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="a9db7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a9db7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9db7-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="a9db7-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="a9db7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a9db7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9db7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a9db7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a9db7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a9db7-112">Area:</span></span>  <br/> |<span data-ttu-id="a9db7-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="a9db7-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9db7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9db7-114">Remarks</span></span>

<span data-ttu-id="a9db7-115">Это свойство представляет свойство каждого получателя на отчеты о доставке и недоставке и свойства каждого сообщения на чтение и nonread отчетов.</span><span class="sxs-lookup"><span data-stu-id="a9db7-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a9db7-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a9db7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9db7-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a9db7-117">Protocol specifications</span></span>

<span data-ttu-id="a9db7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9db7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9db7-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a9db7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9db7-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9db7-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9db7-121">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9db7-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="a9db7-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9db7-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9db7-123">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9db7-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9db7-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a9db7-124">Header files</span></span>

<span data-ttu-id="a9db7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9db7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9db7-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a9db7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9db7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9db7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a9db7-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a9db7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9db7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a9db7-129">See also</span></span>



[<span data-ttu-id="a9db7-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a9db7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9db7-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a9db7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9db7-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a9db7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9db7-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a9db7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

