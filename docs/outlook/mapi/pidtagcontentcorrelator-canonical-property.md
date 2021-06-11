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
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438528"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="4f597-103">Каноническое свойство PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="4f597-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="4f597-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f597-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f597-105">Содержит значение, которое отправитель сообщения может использовать для совпадения отчета с исходным сообщением.</span><span class="sxs-lookup"><span data-stu-id="4f597-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f597-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4f597-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f597-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="4f597-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="4f597-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4f597-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f597-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="4f597-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="4f597-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4f597-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f597-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4f597-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4f597-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4f597-112">Area:</span></span>  <br/> |<span data-ttu-id="4f597-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4f597-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f597-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f597-114">Remarks</span></span>

<span data-ttu-id="4f597-115">Содержимое двоичной строки определяется составивщиком сообщений.</span><span class="sxs-lookup"><span data-stu-id="4f597-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="4f597-116">Если задано исходяние сообщения, это свойство должно быть скопировано на любые отчеты, созданные в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="4f597-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f597-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f597-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f597-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4f597-118">Header files</span></span>

<span data-ttu-id="4f597-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f597-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f597-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4f597-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f597-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f597-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4f597-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="4f597-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f597-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4f597-123">See also</span></span>



[<span data-ttu-id="4f597-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f597-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f597-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f597-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f597-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4f597-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f597-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4f597-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

