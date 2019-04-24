---
title: Каноническое свойство PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341960"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="597ef-103">Каноническое свойство PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="597ef-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="597ef-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="597ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="597ef-105">Содержит значение TRUE, если отправитель сообщения запрашивает отчет о недоставке для определенного получателя.</span><span class="sxs-lookup"><span data-stu-id="597ef-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="597ef-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="597ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="597ef-107">ПР_ОРИГИНАТОР_НОН_ДЕЛИВЕРИ_РЕПОРТ_РЕКУЕСТЕД</span><span class="sxs-lookup"><span data-stu-id="597ef-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="597ef-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="597ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="597ef-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="597ef-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="597ef-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="597ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="597ef-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="597ef-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="597ef-112">Область:</span><span class="sxs-lookup"><span data-stu-id="597ef-112">Area:</span></span>  <br/> |<span data-ttu-id="597ef-113">MIME</span><span class="sxs-lookup"><span data-stu-id="597ef-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="597ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="597ef-114">Remarks</span></span>

<span data-ttu-id="597ef-115">Это свойство используется для направления системы обмена сообщениями на обработку недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="597ef-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="597ef-116">В этом случае сообщение должно также иметь свойство **пр_оригинатор_деливери_репорт_рекуестед** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) со значением false.</span><span class="sxs-lookup"><span data-stu-id="597ef-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="597ef-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="597ef-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="597ef-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="597ef-118">Protocol specifications</span></span>

<span data-ttu-id="597ef-119">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="597ef-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="597ef-120">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="597ef-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="597ef-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="597ef-121">Header files</span></span>

<span data-ttu-id="597ef-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="597ef-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="597ef-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="597ef-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="597ef-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="597ef-124">Mapitags.h</span></span>
  
> <span data-ttu-id="597ef-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="597ef-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="597ef-126">См. также</span><span class="sxs-lookup"><span data-stu-id="597ef-126">See also</span></span>



[<span data-ttu-id="597ef-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="597ef-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="597ef-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="597ef-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="597ef-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="597ef-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="597ef-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="597ef-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

