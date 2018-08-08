---
title: Каноническое свойство PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45d8512d48a1908d81e78b87c5975ab2da8c6c80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810434"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="948fb-103">Каноническое свойство PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="948fb-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="948fb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="948fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="948fb-105">Содержит значение для каждого участника, перечисленные в свойстве **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="948fb-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="948fb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="948fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="948fb-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="948fb-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="948fb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="948fb-108">Property set:</span></span>  <br/> |<span data-ttu-id="948fb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="948fb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="948fb-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="948fb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="948fb-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="948fb-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="948fb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="948fb-112">Data type:</span></span>  <br/> |<span data-ttu-id="948fb-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="948fb-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="948fb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="948fb-114">Area:</span></span>  <br/> |<span data-ttu-id="948fb-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="948fb-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="948fb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="948fb-116">Remarks</span></span>

<span data-ttu-id="948fb-117">Это свойство является обязательным только в том случае, если свойство **dispidNonSendableTo** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="948fb-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="948fb-118">Количество значений в это свойство должно быть равно значений в **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="948fb-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="948fb-119">Каждое значение PT_LONG в это свойство соответствует участника в свойстве **dispidNonSendableTo** с таким же индексом.</span><span class="sxs-lookup"><span data-stu-id="948fb-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="948fb-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="948fb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="948fb-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="948fb-121">Protocol specifications</span></span>

<span data-ttu-id="948fb-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="948fb-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="948fb-123">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="948fb-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="948fb-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="948fb-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="948fb-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="948fb-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="948fb-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="948fb-126">Header files</span></span>

<span data-ttu-id="948fb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="948fb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="948fb-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="948fb-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="948fb-129">См. также</span><span class="sxs-lookup"><span data-stu-id="948fb-129">See also</span></span>



[<span data-ttu-id="948fb-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="948fb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="948fb-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="948fb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="948fb-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="948fb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="948fb-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="948fb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

