---
title: Каноническое свойство PidTagReportDispositionMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d598337a4a66b6345b2f7c827b62a2ccd8af366
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428972"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="4baf6-103">Каноническое свойство PidTagReportDispositionMode</span><span class="sxs-lookup"><span data-stu-id="4baf6-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="4baf6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4baf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4baf6-105">Указывает расположение квитанции для сообщений, которые запрашивают квитанции.</span><span class="sxs-lookup"><span data-stu-id="4baf6-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4baf6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4baf6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4baf6-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="4baf6-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="4baf6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4baf6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4baf6-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="4baf6-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="4baf6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4baf6-110">Data type:</span></span>  <br/> |<span data-ttu-id="4baf6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4baf6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4baf6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4baf6-112">Area:</span></span>  <br/> |<span data-ttu-id="4baf6-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="4baf6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4baf6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4baf6-114">Remarks</span></span>

<span data-ttu-id="4baf6-115">Возможные значения этого свойства: manual-action/MDN-sent-automatically и "manual-action/MDN-sent-manually".</span><span class="sxs-lookup"><span data-stu-id="4baf6-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4baf6-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4baf6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4baf6-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4baf6-117">Protocol specifications</span></span>

<span data-ttu-id="4baf6-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="4baf6-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="4baf6-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4baf6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4baf6-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="4baf6-120">Header files</span></span>

<span data-ttu-id="4baf6-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4baf6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4baf6-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4baf6-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4baf6-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4baf6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4baf6-124">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="4baf6-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4baf6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4baf6-125">See also</span></span>



[<span data-ttu-id="4baf6-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4baf6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4baf6-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4baf6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4baf6-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4baf6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4baf6-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4baf6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

