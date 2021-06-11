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
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="2b65e-103">Каноническое свойство PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="2b65e-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2b65e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b65e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b65e-105">Содержит ключ поиска для получателя, который должен получать отчеты для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b65e-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b65e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2b65e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b65e-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2b65e-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2b65e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2b65e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b65e-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="2b65e-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="2b65e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2b65e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b65e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2b65e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2b65e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2b65e-112">Area:</span></span>  <br/> |<span data-ttu-id="2b65e-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="2b65e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b65e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b65e-114">Remarks</span></span>

<span data-ttu-id="2b65e-115">Это свойство является одним из свойств адресов для получателя, делегированного отправителю для получения отчетов, созданных для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b65e-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="2b65e-116">Клиентская заявка, которая должна отправлять отчеты другому пользователю, должна установить это свойство во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b65e-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="2b65e-117">Если она не установлена, отчеты отправляются отправителю сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b65e-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b65e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b65e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b65e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2b65e-119">Protocol specifications</span></span>

<span data-ttu-id="2b65e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b65e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b65e-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2b65e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b65e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b65e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b65e-123">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2b65e-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b65e-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="2b65e-124">Header files</span></span>

<span data-ttu-id="2b65e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b65e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b65e-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2b65e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b65e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b65e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2b65e-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2b65e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b65e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2b65e-129">See also</span></span>



[<span data-ttu-id="2b65e-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b65e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b65e-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b65e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b65e-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2b65e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b65e-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="2b65e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

