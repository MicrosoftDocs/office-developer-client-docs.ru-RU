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
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575457"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="1e7f2-103">Каноническое свойство PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="1e7f2-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="1e7f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e7f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e7f2-105">Содержит значение TRUE, если отправитель сообщения запрашивает взаимосвязи компонентов системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e7f2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1e7f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e7f2-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="1e7f2-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="1e7f2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1e7f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e7f2-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="1e7f2-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="1e7f2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1e7f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e7f2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1e7f2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1e7f2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1e7f2-112">Area:</span></span>  <br/> |<span data-ttu-id="1e7f2-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="1e7f2-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e7f2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e7f2-114">Remarks</span></span>

<span data-ttu-id="1e7f2-115">Это свойство используется для запроса корреляции входящих отчетов с помощью исходного отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="1e7f2-116">Когда поставщика транспорта обнаруживает отправленное сообщение с набором **PR_CORRELATE** значение TRUE, свойство **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) присваивается идентификатор система передачи сообщений для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="1e7f2-117">**PR_CORRELATE** следует использовать с системой обмена сообщениями систем, которые поддерживают корреляции по идентификатору MTS, такие как X.400.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e7f2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e7f2-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1e7f2-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1e7f2-119">Header files</span></span>

<span data-ttu-id="1e7f2-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e7f2-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e7f2-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e7f2-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e7f2-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1e7f2-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="1e7f2-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e7f2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1e7f2-124">See also</span></span>



[<span data-ttu-id="1e7f2-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7f2-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e7f2-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7f2-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e7f2-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7f2-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e7f2-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1e7f2-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

