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
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="b4ca3-103">Каноническое свойство PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b4ca3-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="b4ca3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4ca3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4ca3-105">Содержит дату и время, когда система обмена сообщениями может признать недействительным содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4ca3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b4ca3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4ca3-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="b4ca3-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="b4ca3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b4ca3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4ca3-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="b4ca3-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="b4ca3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b4ca3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4ca3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b4ca3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b4ca3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b4ca3-112">Area:</span></span>  <br/> |<span data-ttu-id="b4ca3-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="b4ca3-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4ca3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4ca3-114">Remarks</span></span>

<span data-ttu-id="b4ca3-115">Это свойство используется для управления системой обмена сообщениями при обработке доставленных межличностных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b4ca3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4ca3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4ca3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b4ca3-117">Protocol specifications</span></span>

<span data-ttu-id="b4ca3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4ca3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4ca3-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4ca3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4ca3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4ca3-121">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4ca3-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b4ca3-122">Header files</span></span>

<span data-ttu-id="b4ca3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4ca3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4ca3-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4ca3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4ca3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b4ca3-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4ca3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b4ca3-127">See also</span></span>



[<span data-ttu-id="b4ca3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b4ca3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4ca3-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b4ca3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4ca3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b4ca3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4ca3-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b4ca3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

