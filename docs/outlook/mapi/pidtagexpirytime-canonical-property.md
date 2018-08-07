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
ms.openlocfilehash: 4666a5837c9f9f2ceb209088929aa3d343eb02f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811128"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="d4681-103">Каноническое свойство PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d4681-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="d4681-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4681-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4681-105">Содержит дату и время, когда система обмена сообщениями можно объявить недействительным содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="d4681-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4681-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d4681-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4681-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="d4681-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="d4681-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d4681-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4681-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="d4681-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="d4681-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d4681-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4681-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d4681-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d4681-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d4681-112">Area:</span></span>  <br/> |<span data-ttu-id="d4681-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="d4681-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4681-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4681-114">Remarks</span></span>

<span data-ttu-id="d4681-115">Это свойство используется для направления доставку сообщений электронной почты — это системе обмена сообщениями при обработке.</span><span class="sxs-lookup"><span data-stu-id="d4681-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4681-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4681-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4681-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d4681-117">Protocol specifications</span></span>

<span data-ttu-id="d4681-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4681-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4681-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4681-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4681-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4681-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4681-121">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d4681-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4681-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d4681-122">Header files</span></span>

<span data-ttu-id="d4681-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4681-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4681-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d4681-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4681-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4681-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d4681-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d4681-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4681-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d4681-127">See also</span></span>



[<span data-ttu-id="d4681-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4681-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4681-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4681-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4681-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d4681-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4681-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d4681-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

