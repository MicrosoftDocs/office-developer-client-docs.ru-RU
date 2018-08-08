---
title: Каноническое свойство PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 087585e936f04f18ad15f390a083213e2285da83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811108"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="24ce5-103">Каноническое свойство PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="24ce5-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="24ce5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24ce5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24ce5-105">Определяет время отправки истечения срока действия в сочетании со свойством **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="24ce5-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24ce5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="24ce5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24ce5-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="24ce5-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="24ce5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="24ce5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24ce5-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="24ce5-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="24ce5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="24ce5-110">Data type:</span></span>  <br/> |<span data-ttu-id="24ce5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24ce5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24ce5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="24ce5-112">Area:</span></span>  <br/> |<span data-ttu-id="24ce5-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24ce5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="24ce5-114">Remarks</span></span>

<span data-ttu-id="24ce5-115">Это свойство должен иметь значение от 0 до 999 включительно, если он существует.</span><span class="sxs-lookup"><span data-stu-id="24ce5-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24ce5-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="24ce5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24ce5-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="24ce5-117">Protocol specifications</span></span>

<span data-ttu-id="24ce5-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24ce5-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24ce5-119">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24ce5-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24ce5-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="24ce5-120">Header files</span></span>

<span data-ttu-id="24ce5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24ce5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="24ce5-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="24ce5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="24ce5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24ce5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="24ce5-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="24ce5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24ce5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="24ce5-125">See also</span></span>



[<span data-ttu-id="24ce5-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24ce5-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24ce5-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24ce5-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="24ce5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

