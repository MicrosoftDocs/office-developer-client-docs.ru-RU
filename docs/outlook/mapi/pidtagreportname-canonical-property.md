---
title: Каноническое свойство PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569584"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="e82ca-103">Каноническое свойство PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="e82ca-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="e82ca-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e82ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e82ca-105">Содержит отображаемое имя для получателя, должны получить отчеты для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e82ca-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e82ca-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e82ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e82ca-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e82ca-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e82ca-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e82ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e82ca-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="e82ca-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="e82ca-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e82ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="e82ca-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e82ca-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e82ca-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e82ca-112">Area:</span></span>  <br/> |<span data-ttu-id="e82ca-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="e82ca-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e82ca-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e82ca-114">Remarks</span></span>

<span data-ttu-id="e82ca-115">Эти свойства являются примерами свойства адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e82ca-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="e82ca-116">Клиентское приложение, которое направлять отчеты другому пользователю необходимо задать эти свойства во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="e82ca-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="e82ca-117">Если они не заданы, отчеты, передаются в отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="e82ca-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e82ca-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e82ca-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e82ca-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e82ca-119">Header files</span></span>

<span data-ttu-id="e82ca-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e82ca-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e82ca-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e82ca-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e82ca-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e82ca-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e82ca-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e82ca-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e82ca-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e82ca-124">See also</span></span>



[<span data-ttu-id="e82ca-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e82ca-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e82ca-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e82ca-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e82ca-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e82ca-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e82ca-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e82ca-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

