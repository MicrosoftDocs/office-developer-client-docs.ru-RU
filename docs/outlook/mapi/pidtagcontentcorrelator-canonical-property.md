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
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568807"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="41936-103">Каноническое свойство PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="41936-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="41936-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41936-105">Содержит значение, отправителя сообщения можно использовать в соответствии с отчет с исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="41936-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41936-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="41936-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41936-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="41936-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="41936-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="41936-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41936-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="41936-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="41936-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="41936-110">Data type:</span></span>  <br/> |<span data-ttu-id="41936-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="41936-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="41936-112">Область:</span><span class="sxs-lookup"><span data-stu-id="41936-112">Area:</span></span>  <br/> |<span data-ttu-id="41936-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="41936-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41936-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="41936-114">Remarks</span></span>

<span data-ttu-id="41936-115">Содержимое двоичные строки определяются отправителем сообщения.</span><span class="sxs-lookup"><span data-stu-id="41936-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="41936-116">Если набор на исходящие сообщения, это свойство должен быть скопирован на все отчеты, созданные в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="41936-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41936-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41936-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="41936-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="41936-118">Header files</span></span>

<span data-ttu-id="41936-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41936-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="41936-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="41936-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="41936-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41936-121">Mapitags.h</span></span>
  
> <span data-ttu-id="41936-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="41936-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41936-123">См. также</span><span class="sxs-lookup"><span data-stu-id="41936-123">See also</span></span>



[<span data-ttu-id="41936-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41936-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41936-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41936-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41936-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="41936-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41936-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="41936-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

