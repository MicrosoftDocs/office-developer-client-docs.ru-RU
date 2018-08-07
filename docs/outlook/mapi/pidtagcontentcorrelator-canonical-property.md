---
title: Каноническое свойство PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810978"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="6f029-103">Каноническое свойство PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="6f029-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="6f029-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f029-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f029-105">Содержит значение, отправителя сообщения можно использовать в соответствии с отчет с исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f029-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f029-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6f029-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f029-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="6f029-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="6f029-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6f029-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f029-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="6f029-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="6f029-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6f029-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f029-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f029-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f029-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6f029-112">Area:</span></span>  <br/> |<span data-ttu-id="6f029-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="6f029-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f029-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f029-114">Remarks</span></span>

<span data-ttu-id="6f029-115">Содержимое двоичные строки определяются отправителем сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f029-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="6f029-116">Если набор на исходящие сообщения, это свойство должен быть скопирован на все отчеты, созданные в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="6f029-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f029-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6f029-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6f029-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6f029-118">Header files</span></span>

<span data-ttu-id="6f029-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f029-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f029-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6f029-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f029-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f029-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6f029-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6f029-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f029-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6f029-123">See also</span></span>



[<span data-ttu-id="6f029-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f029-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f029-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f029-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f029-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6f029-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f029-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6f029-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

