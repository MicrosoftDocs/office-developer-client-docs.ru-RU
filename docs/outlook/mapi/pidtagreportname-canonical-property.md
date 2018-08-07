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
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811723"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="e2139-103">Каноническое свойство PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="e2139-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="e2139-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2139-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2139-105">Содержит отображаемое имя для получателя, должны получить отчеты для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2139-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2139-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e2139-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2139-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e2139-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e2139-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e2139-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2139-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="e2139-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="e2139-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e2139-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2139-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2139-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2139-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e2139-112">Area:</span></span>  <br/> |<span data-ttu-id="e2139-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="e2139-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2139-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e2139-114">Remarks</span></span>

<span data-ttu-id="e2139-115">Эти свойства являются примерами свойства адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2139-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="e2139-116">Клиентское приложение, которое направлять отчеты другому пользователю необходимо задать эти свойства во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2139-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="e2139-117">Если они не заданы, отчеты, передаются в отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2139-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2139-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e2139-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e2139-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e2139-119">Header files</span></span>

<span data-ttu-id="e2139-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2139-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2139-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e2139-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2139-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2139-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e2139-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e2139-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2139-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e2139-124">See also</span></span>



[<span data-ttu-id="e2139-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e2139-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2139-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e2139-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2139-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e2139-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2139-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e2139-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

