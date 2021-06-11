---
title: Каноническое свойство PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405221"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="d45e4-103">Каноническое свойство PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="d45e4-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="d45e4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d45e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d45e4-105">Содержит TRUE, если отправитель сообщения запрашивает функцию корреляции системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d45e4-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d45e4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d45e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d45e4-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="d45e4-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="d45e4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d45e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d45e4-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="d45e4-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="d45e4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d45e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="d45e4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d45e4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d45e4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d45e4-112">Area:</span></span>  <br/> |<span data-ttu-id="d45e4-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="d45e4-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d45e4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d45e4-114">Remarks</span></span>

<span data-ttu-id="d45e4-115">Это свойство используется для запроса корреляции входящих отчетов с исходным отправленным сообщением.</span><span class="sxs-lookup"><span data-stu-id="d45e4-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="d45e4-116">Когда поставщик транспорта сталкивается с  отправленным сообщением с PR_CORRELATE для true, он задает свойство **PR_CORRELATE_MTSID** [(PidTagCorrelateMtsid)](pidtagcorrelatemtsid-canonical-property.md)для идентификатора системы передачи сообщений (MTS) для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d45e4-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="d45e4-117">**PR_CORRELATE** следует использовать с системами обмена сообщениями, поддерживаюми корреляцию идентификатора МТС, например X.400.</span><span class="sxs-lookup"><span data-stu-id="d45e4-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d45e4-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d45e4-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d45e4-119">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d45e4-119">Header files</span></span>

<span data-ttu-id="d45e4-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d45e4-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="d45e4-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d45e4-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="d45e4-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d45e4-122">Mapitags.h</span></span>
  
> <span data-ttu-id="d45e4-123">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="d45e4-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d45e4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d45e4-124">See also</span></span>



[<span data-ttu-id="d45e4-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d45e4-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d45e4-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d45e4-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d45e4-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d45e4-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d45e4-128">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d45e4-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

