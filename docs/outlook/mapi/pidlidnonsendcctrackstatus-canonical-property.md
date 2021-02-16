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
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="3d36e-103">Каноническое свойство PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="3d36e-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3d36e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d36e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d36e-105">Содержит значение для каждого участника, перечисленного в свойстве **dispidNonSendableCC** ([PidLidNonSendableCc).](pidlidnonsendablecc-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3d36e-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d36e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3d36e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d36e-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="3d36e-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="3d36e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3d36e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3d36e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3d36e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3d36e-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="3d36e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3d36e-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="3d36e-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="3d36e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3d36e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3d36e-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="3d36e-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="3d36e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3d36e-114">Area:</span></span>  <br/> |<span data-ttu-id="3d36e-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="3d36e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d36e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d36e-116">Remarks</span></span>

<span data-ttu-id="3d36e-117">Это свойство необходимо, только если задано свойство **dispidNonSendableCC.**</span><span class="sxs-lookup"><span data-stu-id="3d36e-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="3d36e-118">Число значений в этом свойстве должно быть равно числу значений **в dispidNonSendableCC.**</span><span class="sxs-lookup"><span data-stu-id="3d36e-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="3d36e-119">Каждое PT_LONG в этом свойстве соответствует участнику в свойстве **dispidNonSendableCC** с одинаковым индексом.</span><span class="sxs-lookup"><span data-stu-id="3d36e-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d36e-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d36e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d36e-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3d36e-121">Protocol specifications</span></span>

<span data-ttu-id="3d36e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d36e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d36e-123">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="3d36e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d36e-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d36e-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d36e-125">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d36e-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d36e-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3d36e-126">Header files</span></span>

<span data-ttu-id="3d36e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d36e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d36e-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3d36e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d36e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3d36e-129">See also</span></span>



[<span data-ttu-id="3d36e-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d36e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d36e-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d36e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d36e-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3d36e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d36e-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3d36e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

