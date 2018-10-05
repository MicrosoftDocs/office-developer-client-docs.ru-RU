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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398026"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="dc71e-103">Каноническое свойство PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="dc71e-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="dc71e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc71e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc71e-105">Содержит номер, который можно использовать для вычисления отсрочке отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="dc71e-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc71e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dc71e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc71e-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="dc71e-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="dc71e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dc71e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc71e-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="dc71e-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="dc71e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dc71e-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc71e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc71e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc71e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dc71e-112">Area:</span></span>  <br/> |<span data-ttu-id="dc71e-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="dc71e-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc71e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc71e-114">Remarks</span></span>

<span data-ttu-id="dc71e-115">Это свойство используется для вычисления свойство **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)), когда она не существует.</span><span class="sxs-lookup"><span data-stu-id="dc71e-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="dc71e-116">При отложенной отправки сообщения свойство **PR_DEFERRED_SEND_NUMBER** должно быть установлено вместе со свойством **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), если свойство **PR_DEFERRED_SEND_TIME** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dc71e-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="dc71e-117">**PR_DEFERRED_SEND_NUMBER** должен иметь значение от 0 до 999.</span><span class="sxs-lookup"><span data-stu-id="dc71e-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc71e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc71e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc71e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dc71e-119">Protocol specifications</span></span>

<span data-ttu-id="dc71e-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc71e-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc71e-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dc71e-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc71e-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dc71e-122">Header files</span></span>

<span data-ttu-id="dc71e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc71e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc71e-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dc71e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc71e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc71e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="dc71e-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="dc71e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc71e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dc71e-127">See also</span></span>



[<span data-ttu-id="dc71e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc71e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc71e-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc71e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc71e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dc71e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc71e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dc71e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

