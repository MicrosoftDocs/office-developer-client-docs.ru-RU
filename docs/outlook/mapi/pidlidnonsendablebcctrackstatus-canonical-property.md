---
title: Каноническое свойство PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de3c56e3ed532d8f4c3cff272049384e9c6a3867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586090"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="93d10-103">Каноническое свойство PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="93d10-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="93d10-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93d10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93d10-105">Содержит значение для каждого участника, указанный в свойстве **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="93d10-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93d10-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="93d10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93d10-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="93d10-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="93d10-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="93d10-108">Property set:</span></span>  <br/> |<span data-ttu-id="93d10-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="93d10-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="93d10-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="93d10-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="93d10-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="93d10-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="93d10-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="93d10-112">Data type:</span></span>  <br/> |<span data-ttu-id="93d10-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="93d10-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="93d10-114">Область:</span><span class="sxs-lookup"><span data-stu-id="93d10-114">Area:</span></span>  <br/> |<span data-ttu-id="93d10-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="93d10-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93d10-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="93d10-116">Remarks</span></span>

<span data-ttu-id="93d10-117">Это свойство является обязательным только в том случае, если свойство **dispidNonSendableBCC** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="93d10-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="93d10-118">Количество значений в это свойство должно быть равно значений в **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="93d10-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="93d10-119">Каждое значение в это свойство соответствует участника в свойстве **dispidNonSendableBCC** с таким же индексом.</span><span class="sxs-lookup"><span data-stu-id="93d10-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93d10-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93d10-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93d10-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="93d10-121">Protocol specifications</span></span>

<span data-ttu-id="93d10-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93d10-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93d10-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="93d10-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93d10-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93d10-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93d10-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="93d10-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93d10-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="93d10-126">Header files</span></span>

<span data-ttu-id="93d10-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93d10-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="93d10-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="93d10-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93d10-129">См. также</span><span class="sxs-lookup"><span data-stu-id="93d10-129">See also</span></span>



[<span data-ttu-id="93d10-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93d10-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93d10-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93d10-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93d10-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="93d10-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93d10-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="93d10-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

