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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359180"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="0edd9-103">Каноническое свойство PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="0edd9-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0edd9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0edd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0edd9-105">Содержит ключ поиска для получателя, который должен получить отчеты для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="0edd9-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0edd9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0edd9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0edd9-107">ПР_РЕПОРТ_СЕАРЧ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="0edd9-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0edd9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0edd9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0edd9-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="0edd9-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="0edd9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0edd9-110">Data type:</span></span>  <br/> |<span data-ttu-id="0edd9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0edd9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0edd9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0edd9-112">Area:</span></span>  <br/> |<span data-ttu-id="0edd9-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="0edd9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0edd9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0edd9-114">Remarks</span></span>

<span data-ttu-id="0edd9-115">Это свойство является одним из свойств адреса получателя, которому отправитель делегирован, чтобы получать отчеты, созданные для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="0edd9-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="0edd9-116">Клиентское приложение, которое должно маршрутизировать отчеты другому пользователю, должно устанавливать это свойство во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="0edd9-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="0edd9-117">Если он не задан, отчеты отправляются отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="0edd9-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0edd9-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0edd9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0edd9-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0edd9-119">Protocol specifications</span></span>

<span data-ttu-id="0edd9-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edd9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edd9-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0edd9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0edd9-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edd9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edd9-123">Задает свойства и операции, допустимые для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0edd9-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0edd9-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0edd9-124">Header files</span></span>

<span data-ttu-id="0edd9-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0edd9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0edd9-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0edd9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0edd9-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0edd9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0edd9-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="0edd9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0edd9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0edd9-129">See also</span></span>



[<span data-ttu-id="0edd9-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0edd9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0edd9-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0edd9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0edd9-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0edd9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0edd9-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0edd9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

