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
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335429"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="b6d61-103">Каноническое свойство PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="b6d61-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="b6d61-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6d61-105">Содержит отображаемое имя получателя, который должен получить отчеты для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6d61-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6d61-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b6d61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6d61-107">ПР_РЕПОРТ_НАМЕ, ПР_РЕПОРТ_НАМЕ_А, ПР_РЕПОРТ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="b6d61-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b6d61-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b6d61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6d61-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="b6d61-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="b6d61-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b6d61-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6d61-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="b6d61-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b6d61-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b6d61-112">Area:</span></span>  <br/> |<span data-ttu-id="b6d61-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d61-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6d61-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6d61-114">Remarks</span></span>

<span data-ttu-id="b6d61-115">Эти свойства являются примерами свойств адреса получателя, которым отправитель делегирован для получения любых отчетов, созданных для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6d61-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="b6d61-116">Клиентское приложение, которое должно маршрутизировать отчеты другому пользователю, должно задавать эти свойства во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6d61-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="b6d61-117">Если они не заданы, отчеты отправляются отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6d61-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6d61-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b6d61-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b6d61-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b6d61-119">Header files</span></span>

<span data-ttu-id="b6d61-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b6d61-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6d61-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b6d61-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6d61-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b6d61-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b6d61-123">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b6d61-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6d61-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b6d61-124">See also</span></span>



[<span data-ttu-id="b6d61-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d61-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6d61-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d61-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6d61-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d61-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6d61-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b6d61-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

