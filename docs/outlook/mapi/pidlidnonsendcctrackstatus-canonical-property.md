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
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319672"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="327b0-103">Каноническое свойство PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="327b0-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="327b0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="327b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="327b0-105">Содержит значение для каждого участника, указанного в свойстве **диспиднонсендаблекк** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="327b0-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="327b0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="327b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="327b0-107">Диспиднонсендкктраккстатус</span><span class="sxs-lookup"><span data-stu-id="327b0-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="327b0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="327b0-108">Property set:</span></span>  <br/> |<span data-ttu-id="327b0-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="327b0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="327b0-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="327b0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="327b0-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="327b0-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="327b0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="327b0-112">Data type:</span></span>  <br/> |<span data-ttu-id="327b0-113">ПТ_МВ_ЛОНГ</span><span class="sxs-lookup"><span data-stu-id="327b0-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="327b0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="327b0-114">Area:</span></span>  <br/> |<span data-ttu-id="327b0-115">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="327b0-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="327b0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="327b0-116">Remarks</span></span>

<span data-ttu-id="327b0-117">Это свойство является обязательным только в том случае, если задано свойство **диспиднонсендаблекк** .</span><span class="sxs-lookup"><span data-stu-id="327b0-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="327b0-118">Количество значений в этом свойстве должно равняться количеству значений в **диспиднонсендаблекк**.</span><span class="sxs-lookup"><span data-stu-id="327b0-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="327b0-119">Каждое значение ПТ_ЛОНГ в этом свойстве соответствует участнику в свойстве **диспиднонсендаблекк** в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="327b0-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="327b0-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="327b0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="327b0-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="327b0-121">Protocol specifications</span></span>

<span data-ttu-id="327b0-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="327b0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="327b0-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="327b0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="327b0-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="327b0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="327b0-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="327b0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="327b0-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="327b0-126">Header files</span></span>

<span data-ttu-id="327b0-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="327b0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="327b0-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="327b0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="327b0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="327b0-129">See also</span></span>



[<span data-ttu-id="327b0-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="327b0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="327b0-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="327b0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="327b0-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="327b0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="327b0-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="327b0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

