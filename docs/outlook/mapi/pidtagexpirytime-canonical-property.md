---
title: Каноническое свойство PidTagExpiryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316375"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="65270-103">Каноническое свойство PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="65270-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="65270-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65270-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65270-105">Содержит дату и время, когда система обмена сообщениями может сделать недействительным содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="65270-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65270-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="65270-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65270-107">ПР_ЕКСПИРИ_ТИМЕ</span><span class="sxs-lookup"><span data-stu-id="65270-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="65270-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="65270-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65270-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="65270-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="65270-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="65270-110">Data type:</span></span>  <br/> |<span data-ttu-id="65270-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="65270-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="65270-112">Область:</span><span class="sxs-lookup"><span data-stu-id="65270-112">Area:</span></span>  <br/> |<span data-ttu-id="65270-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="65270-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65270-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="65270-114">Remarks</span></span>

<span data-ttu-id="65270-115">Это свойство используется для направления системы обмена сообщениями в обработку доставленных взаимонаправленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="65270-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="65270-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="65270-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65270-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="65270-117">Protocol specifications</span></span>

<span data-ttu-id="65270-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65270-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65270-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="65270-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65270-120">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65270-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65270-121">Задает свойства и операции, допустимые для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="65270-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65270-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="65270-122">Header files</span></span>

<span data-ttu-id="65270-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="65270-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="65270-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="65270-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="65270-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="65270-125">Mapitags.h</span></span>
  
> <span data-ttu-id="65270-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="65270-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65270-127">См. также</span><span class="sxs-lookup"><span data-stu-id="65270-127">See also</span></span>



[<span data-ttu-id="65270-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="65270-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65270-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="65270-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65270-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="65270-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65270-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="65270-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

