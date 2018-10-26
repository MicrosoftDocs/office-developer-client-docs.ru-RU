---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582884"
---
# <a name="fbadproptag"></a><span data-ttu-id="cf11d-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="cf11d-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="cf11d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf11d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf11d-105">Проверяет тег указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="cf11d-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf11d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cf11d-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf11d-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="cf11d-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="cf11d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cf11d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf11d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf11d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf11d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cf11d-110">Called by:</span></span>  <br/> |<span data-ttu-id="cf11d-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="cf11d-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="cf11d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf11d-112">Parameters</span></span>

 <span data-ttu-id="cf11d-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="cf11d-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="cf11d-114">[in] Свойство tag для проверки.</span><span class="sxs-lookup"><span data-stu-id="cf11d-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf11d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf11d-115">Return value</span></span>

<span data-ttu-id="cf11d-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf11d-116">TRUE</span></span> 
  
> <span data-ttu-id="cf11d-117">Тег указанное свойство не является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="cf11d-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="cf11d-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf11d-118">FALSE</span></span> 
  
> <span data-ttu-id="cf11d-119">Тег указанное свойство является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="cf11d-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf11d-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf11d-120">Remarks</span></span>

<span data-ttu-id="cf11d-121">Функция **FBadPropTag** проверяет указанное свойство tag, на основе MAPI определений.</span><span class="sxs-lookup"><span data-stu-id="cf11d-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="cf11d-122">Он сделать sures, тип свойства — это один из типов, определенных параметром MAPI, который идентификатор свойства определяется как этого типа.</span><span class="sxs-lookup"><span data-stu-id="cf11d-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf11d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cf11d-123">See also</span></span>



[<span data-ttu-id="cf11d-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="cf11d-124">FBadProp</span></span>](fbadprop.md)

