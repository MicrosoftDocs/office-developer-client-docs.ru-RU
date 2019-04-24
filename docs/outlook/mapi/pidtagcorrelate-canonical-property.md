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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357920"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="70b04-103">Каноническое свойство PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="70b04-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="70b04-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70b04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70b04-105">Содержит значение TRUE, если отправитель сообщения запрашивает функцию корреляции системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="70b04-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70b04-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="70b04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70b04-107">ПР_КОРРЕЛАТЕ</span><span class="sxs-lookup"><span data-stu-id="70b04-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="70b04-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="70b04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70b04-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="70b04-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="70b04-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="70b04-110">Data type:</span></span>  <br/> |<span data-ttu-id="70b04-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="70b04-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="70b04-112">Область:</span><span class="sxs-lookup"><span data-stu-id="70b04-112">Area:</span></span>  <br/> |<span data-ttu-id="70b04-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="70b04-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70b04-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="70b04-114">Remarks</span></span>

<span data-ttu-id="70b04-115">Это свойство используется для запроса корреляции входящих отчетов с исходным отправленным сообщением.</span><span class="sxs-lookup"><span data-stu-id="70b04-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="70b04-116">Когда поставщик транспорта обнаруживает отправленное сообщение с **пр_коррелате** , для которого ЗАДАНО значение true, он задает для свойства **пр_коррелате_мтсид** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) идентификатор системы передачи сообщений (MTS) для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="70b04-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="70b04-117">**Пр_коррелате** следует использовать с системами обмена сообщениями, поддерживающими корреляцию по идентификатору MTS, например X. 400.</span><span class="sxs-lookup"><span data-stu-id="70b04-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70b04-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="70b04-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="70b04-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="70b04-119">Header files</span></span>

<span data-ttu-id="70b04-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="70b04-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="70b04-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="70b04-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="70b04-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="70b04-122">Mapitags.h</span></span>
  
> <span data-ttu-id="70b04-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="70b04-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70b04-124">См. также</span><span class="sxs-lookup"><span data-stu-id="70b04-124">See also</span></span>



[<span data-ttu-id="70b04-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70b04-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70b04-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="70b04-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70b04-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="70b04-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70b04-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="70b04-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

