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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422315"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="02dbe-103">Каноническое свойство PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="02dbe-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="02dbe-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02dbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02dbe-105">Содержит отображаемую имя получателя, который должен получить отчеты для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="02dbe-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02dbe-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02dbe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02dbe-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="02dbe-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="02dbe-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="02dbe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02dbe-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="02dbe-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="02dbe-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02dbe-110">Data type:</span></span>  <br/> |<span data-ttu-id="02dbe-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="02dbe-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="02dbe-112">Область:</span><span class="sxs-lookup"><span data-stu-id="02dbe-112">Area:</span></span>  <br/> |<span data-ttu-id="02dbe-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="02dbe-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02dbe-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="02dbe-114">Remarks</span></span>

<span data-ttu-id="02dbe-115">Эти свойства являются примерами свойств адреса получателя, делегированного отправителю для получения отчетов, созданных для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="02dbe-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="02dbe-116">Клиентские приложения, которые должны отправлять отчеты другому пользователю, должно устанавливать эти свойства во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="02dbe-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="02dbe-117">Если они не за установлены, отчеты отправляются отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="02dbe-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02dbe-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02dbe-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="02dbe-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="02dbe-119">Header files</span></span>

<span data-ttu-id="02dbe-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02dbe-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="02dbe-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02dbe-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="02dbe-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02dbe-122">Mapitags.h</span></span>
  
> <span data-ttu-id="02dbe-123">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="02dbe-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02dbe-124">См. также</span><span class="sxs-lookup"><span data-stu-id="02dbe-124">See also</span></span>



[<span data-ttu-id="02dbe-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02dbe-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02dbe-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02dbe-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02dbe-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02dbe-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02dbe-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="02dbe-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

