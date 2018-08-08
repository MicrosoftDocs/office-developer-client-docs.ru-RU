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
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808416"
---
# <a name="fbadproptag"></a><span data-ttu-id="17fe3-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="17fe3-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="17fe3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17fe3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17fe3-105">Проверяет тег указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="17fe3-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17fe3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="17fe3-106">Header file:</span></span>  <br/> |<span data-ttu-id="17fe3-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="17fe3-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="17fe3-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="17fe3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="17fe3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="17fe3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="17fe3-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="17fe3-110">Called by:</span></span>  <br/> |<span data-ttu-id="17fe3-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="17fe3-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="17fe3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="17fe3-112">Parameters</span></span>

 <span data-ttu-id="17fe3-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="17fe3-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="17fe3-114">[in] Свойство tag для проверки.</span><span class="sxs-lookup"><span data-stu-id="17fe3-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17fe3-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="17fe3-115">Return value</span></span>

<span data-ttu-id="17fe3-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="17fe3-116">TRUE</span></span> 
  
> <span data-ttu-id="17fe3-117">Тег указанное свойство не является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="17fe3-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="17fe3-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="17fe3-118">FALSE</span></span> 
  
> <span data-ttu-id="17fe3-119">Тег указанное свойство является допустимым тегом свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="17fe3-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17fe3-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="17fe3-120">Remarks</span></span>

<span data-ttu-id="17fe3-121">Функция **FBadPropTag** проверяет указанное свойство tag, на основе MAPI определений.</span><span class="sxs-lookup"><span data-stu-id="17fe3-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="17fe3-122">Он сделать sures, тип свойства — это один из типов, определенных параметром MAPI, который идентификатор свойства определяется как этого типа.</span><span class="sxs-lookup"><span data-stu-id="17fe3-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17fe3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="17fe3-123">See also</span></span>



[<span data-ttu-id="17fe3-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="17fe3-124">FBadProp</span></span>](fbadprop.md)

