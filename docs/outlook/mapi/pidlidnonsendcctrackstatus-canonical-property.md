---
title: Каноническое свойство PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ee68f0f60f96798130115cbd313f6d7cd403486
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590500"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="52985-103">Каноническое свойство PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="52985-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="52985-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52985-105">Содержит значение для каждого участника, перечисленные в свойстве **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52985-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52985-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="52985-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52985-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="52985-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="52985-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="52985-108">Property set:</span></span>  <br/> |<span data-ttu-id="52985-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="52985-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="52985-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="52985-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="52985-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="52985-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="52985-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="52985-112">Data type:</span></span>  <br/> |<span data-ttu-id="52985-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="52985-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="52985-114">Область:</span><span class="sxs-lookup"><span data-stu-id="52985-114">Area:</span></span>  <br/> |<span data-ttu-id="52985-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="52985-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52985-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="52985-116">Remarks</span></span>

<span data-ttu-id="52985-117">Это свойство является обязательным только в том случае, если свойство **dispidNonSendableCC** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="52985-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="52985-118">Количество значений в это свойство должно быть равно значений в **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="52985-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="52985-119">Каждое значение PT_LONG в это свойство соответствует участника в свойстве **dispidNonSendableCC** с таким же индексом.</span><span class="sxs-lookup"><span data-stu-id="52985-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52985-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="52985-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52985-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="52985-121">Protocol specifications</span></span>

<span data-ttu-id="52985-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52985-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52985-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="52985-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52985-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52985-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52985-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="52985-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52985-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="52985-126">Header files</span></span>

<span data-ttu-id="52985-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52985-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="52985-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="52985-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52985-129">См. также</span><span class="sxs-lookup"><span data-stu-id="52985-129">See also</span></span>



[<span data-ttu-id="52985-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="52985-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52985-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="52985-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52985-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="52985-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52985-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="52985-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

