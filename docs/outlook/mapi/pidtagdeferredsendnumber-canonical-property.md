---
title: Каноническое свойство PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357738"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="45ff6-103">Каноническое свойство PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="45ff6-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="45ff6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45ff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45ff6-105">Содержит номер, который можно использовать для вычисления отсрочки отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="45ff6-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45ff6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="45ff6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45ff6-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="45ff6-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="45ff6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="45ff6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45ff6-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="45ff6-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="45ff6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="45ff6-110">Data type:</span></span>  <br/> |<span data-ttu-id="45ff6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45ff6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45ff6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="45ff6-112">Area:</span></span>  <br/> |<span data-ttu-id="45ff6-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="45ff6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45ff6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="45ff6-114">Remarks</span></span>

<span data-ttu-id="45ff6-115">Это свойство используется для вычисления **свойства PR_DEFERRED_SEND_TIME** [(PidTagDeferredSendTime),](pidtagdeferredsendtime-canonical-property.md)когда оно не присутствует.</span><span class="sxs-lookup"><span data-stu-id="45ff6-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="45ff6-116">При отложении отправки  сообщения свойство PR_DEFERRED_SEND_NUMBER должно быть задано вместе с свойством **PR_DEFERRED_SEND_UNITS** [(PidTagDeferredSendUnits),](pidtagdeferredsendunits-canonical-property.md)если свойство PR_DEFERRED_SEND_TIME отсутствует. </span><span class="sxs-lookup"><span data-stu-id="45ff6-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="45ff6-117">Значение **PR_DEFERRED_SEND_NUMBER** должно быть установлено между 0 и 999.</span><span class="sxs-lookup"><span data-stu-id="45ff6-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="45ff6-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="45ff6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45ff6-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="45ff6-119">Protocol specifications</span></span>

<span data-ttu-id="45ff6-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45ff6-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45ff6-121">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="45ff6-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45ff6-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="45ff6-122">Header files</span></span>

<span data-ttu-id="45ff6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45ff6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="45ff6-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="45ff6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="45ff6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45ff6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="45ff6-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="45ff6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45ff6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="45ff6-127">See also</span></span>



[<span data-ttu-id="45ff6-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="45ff6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45ff6-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="45ff6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45ff6-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="45ff6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45ff6-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="45ff6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

