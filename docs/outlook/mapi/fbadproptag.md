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
# <a name="fbadproptag"></a><span data-ttu-id="62a94-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="62a94-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="62a94-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62a94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62a94-105">Проверяет тег указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="62a94-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62a94-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="62a94-106">Header file:</span></span>  <br/> |<span data-ttu-id="62a94-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="62a94-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="62a94-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="62a94-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="62a94-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="62a94-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="62a94-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="62a94-110">Called by:</span></span>  <br/> |<span data-ttu-id="62a94-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="62a94-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="62a94-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="62a94-112">Parameters</span></span>

 <span data-ttu-id="62a94-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="62a94-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="62a94-114">[in] Свойство tag для проверки.</span><span class="sxs-lookup"><span data-stu-id="62a94-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62a94-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="62a94-115">Return value</span></span>

<span data-ttu-id="62a94-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="62a94-116">TRUE</span></span> 
  
> <span data-ttu-id="62a94-117">Тег указанное свойство не является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="62a94-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="62a94-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="62a94-118">FALSE</span></span> 
  
> <span data-ttu-id="62a94-119">Тег указанное свойство является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="62a94-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62a94-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="62a94-120">Remarks</span></span>

<span data-ttu-id="62a94-121">Функция **FBadPropTag** проверяет указанное свойство tag, на основе MAPI определений.</span><span class="sxs-lookup"><span data-stu-id="62a94-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="62a94-122">Он сделать sures, тип свойства — это один из типов, определенных параметром MAPI, который идентификатор свойства определяется как этого типа.</span><span class="sxs-lookup"><span data-stu-id="62a94-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62a94-123">См. также</span><span class="sxs-lookup"><span data-stu-id="62a94-123">See also</span></span>



[<span data-ttu-id="62a94-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="62a94-124">FBadProp</span></span>](fbadprop.md)

