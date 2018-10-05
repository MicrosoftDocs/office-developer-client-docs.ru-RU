---
title: Каноническое свойство PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383508"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="ce449-103">Каноническое свойство PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="ce449-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ce449-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce449-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce449-105">Содержит ключ поиска для получателя, должны получить отчеты для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce449-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce449-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ce449-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce449-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ce449-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ce449-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ce449-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce449-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="ce449-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="ce449-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ce449-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce449-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce449-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce449-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ce449-112">Area:</span></span>  <br/> |<span data-ttu-id="ce449-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="ce449-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce449-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ce449-114">Remarks</span></span>

<span data-ttu-id="ce449-115">Это свойство является одним из свойств адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce449-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="ce449-116">Клиентское приложение, которое направлять отчеты другому пользователю следует устанавливать это свойство во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce449-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="ce449-117">Если не указано, отчеты, передаются в отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce449-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ce449-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ce449-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce449-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ce449-119">Protocol specifications</span></span>

<span data-ttu-id="ce449-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce449-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce449-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ce449-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce449-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce449-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce449-123">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ce449-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce449-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ce449-124">Header files</span></span>

<span data-ttu-id="ce449-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce449-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce449-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ce449-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce449-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce449-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ce449-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ce449-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce449-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ce449-129">See also</span></span>



[<span data-ttu-id="ce449-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce449-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce449-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce449-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce449-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ce449-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce449-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ce449-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

