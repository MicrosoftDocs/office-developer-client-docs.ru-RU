---
title: Каноническое свойство PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811715"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="26b55-103">Каноническое свойство PidTagReportEntryId</span><span class="sxs-lookup"><span data-stu-id="26b55-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="26b55-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26b55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26b55-105">Содержит идентификатор записи для получателя, которые должны получить отчеты для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="26b55-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26b55-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="26b55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26b55-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="26b55-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="26b55-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="26b55-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26b55-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="26b55-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="26b55-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="26b55-110">Data type:</span></span>  <br/> |<span data-ttu-id="26b55-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="26b55-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="26b55-112">Область:</span><span class="sxs-lookup"><span data-stu-id="26b55-112">Area:</span></span>  <br/> |<span data-ttu-id="26b55-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="26b55-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26b55-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="26b55-114">Remarks</span></span>

<span data-ttu-id="26b55-115">Это свойство является одним из свойств адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="26b55-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="26b55-116">Клиентское приложение, которое направлять отчеты другому пользователю следует устанавливать это свойство во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="26b55-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="26b55-117">Если не указано, отчеты, передаются в отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="26b55-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26b55-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="26b55-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26b55-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="26b55-119">Protocol specifications</span></span>

<span data-ttu-id="26b55-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26b55-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26b55-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="26b55-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26b55-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26b55-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26b55-123">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="26b55-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26b55-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="26b55-124">Header files</span></span>

<span data-ttu-id="26b55-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26b55-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="26b55-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="26b55-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="26b55-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26b55-127">Mapitags.h</span></span>
  
> <span data-ttu-id="26b55-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="26b55-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26b55-129">См. также</span><span class="sxs-lookup"><span data-stu-id="26b55-129">See also</span></span>



[<span data-ttu-id="26b55-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="26b55-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26b55-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="26b55-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26b55-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="26b55-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26b55-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="26b55-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

