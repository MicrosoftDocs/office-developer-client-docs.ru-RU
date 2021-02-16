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
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316368"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="af50a-103">Каноническое свойство PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="af50a-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="af50a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af50a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af50a-105">Определяет время отправки с истечением срока действия в сочетании со **свойством PR_EXPIRY_UNITS** ([PidTagExpiryUnits).](pidtagexpiryunits-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af50a-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af50a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af50a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af50a-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="af50a-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="af50a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="af50a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af50a-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="af50a-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="af50a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af50a-110">Data type:</span></span>  <br/> |<span data-ttu-id="af50a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af50a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af50a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="af50a-112">Area:</span></span>  <br/> |<span data-ttu-id="af50a-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="af50a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af50a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="af50a-114">Remarks</span></span>

<span data-ttu-id="af50a-115">Значение этого свойства должно быть установлено от 0 до 999 включительно, если оно присутствует.</span><span class="sxs-lookup"><span data-stu-id="af50a-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af50a-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af50a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af50a-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af50a-117">Protocol specifications</span></span>

<span data-ttu-id="af50a-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af50a-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af50a-119">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="af50a-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af50a-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="af50a-120">Header files</span></span>

<span data-ttu-id="af50a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af50a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="af50a-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af50a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="af50a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af50a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="af50a-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="af50a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af50a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="af50a-125">See also</span></span>



[<span data-ttu-id="af50a-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af50a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af50a-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af50a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af50a-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af50a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af50a-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af50a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

