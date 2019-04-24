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
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341001"
---
# <a name="fbadproptag"></a><span data-ttu-id="33564-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="33564-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="33564-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33564-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33564-105">Проверяет указанный тег свойства.</span><span class="sxs-lookup"><span data-stu-id="33564-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33564-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="33564-106">Header file:</span></span>  <br/> |<span data-ttu-id="33564-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="33564-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="33564-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="33564-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="33564-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="33564-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="33564-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="33564-110">Called by:</span></span>  <br/> |<span data-ttu-id="33564-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="33564-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="33564-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="33564-112">Parameters</span></span>

 <span data-ttu-id="33564-113">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="33564-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="33564-114">возврата Тег свойства, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="33564-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33564-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33564-115">Return value</span></span>

<span data-ttu-id="33564-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="33564-116">TRUE</span></span> 
  
> <span data-ttu-id="33564-117">Указанный тег свойства не является допустимым тегом свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="33564-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="33564-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="33564-118">FALSE</span></span> 
  
> <span data-ttu-id="33564-119">Указанный тег свойства является допустимым тегом свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="33564-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33564-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33564-120">Remarks</span></span>

<span data-ttu-id="33564-121">Функция **фбадпроптаг** проверяет заданный тег свойства на основе определений MAPI.</span><span class="sxs-lookup"><span data-stu-id="33564-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="33564-122">Он гарантирует, что тип свойства является одним из типов, определенных MAPI, и что идентификатор свойства определен как тип этого типа.</span><span class="sxs-lookup"><span data-stu-id="33564-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33564-123">См. также</span><span class="sxs-lookup"><span data-stu-id="33564-123">See also</span></span>



[<span data-ttu-id="33564-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="33564-124">FBadProp</span></span>](fbadprop.md)

