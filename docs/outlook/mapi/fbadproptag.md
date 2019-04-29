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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433649"
---
# <a name="fbadproptag"></a><span data-ttu-id="df0a4-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="df0a4-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="df0a4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df0a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df0a4-105">Проверяет указанный тег свойства.</span><span class="sxs-lookup"><span data-stu-id="df0a4-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df0a4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="df0a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="df0a4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="df0a4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="df0a4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="df0a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="df0a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="df0a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="df0a4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="df0a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="df0a4-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="df0a4-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="df0a4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="df0a4-112">Parameters</span></span>

 <span data-ttu-id="df0a4-113">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="df0a4-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="df0a4-114">возврата Тег свойства, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="df0a4-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df0a4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df0a4-115">Return value</span></span>

<span data-ttu-id="df0a4-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="df0a4-116">TRUE</span></span> 
  
> <span data-ttu-id="df0a4-117">Указанный тег свойства не является допустимым тегом свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="df0a4-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="df0a4-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="df0a4-118">FALSE</span></span> 
  
> <span data-ttu-id="df0a4-119">Указанный тег свойства является допустимым тегом свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="df0a4-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df0a4-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="df0a4-120">Remarks</span></span>

<span data-ttu-id="df0a4-121">Функция **фбадпроптаг** проверяет заданный тег свойства на основе определений MAPI.</span><span class="sxs-lookup"><span data-stu-id="df0a4-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="df0a4-122">Он гарантирует, что тип свойства является одним из типов, определенных MAPI, и что идентификатор свойства определен как тип этого типа.</span><span class="sxs-lookup"><span data-stu-id="df0a4-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df0a4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="df0a4-123">See also</span></span>



[<span data-ttu-id="df0a4-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="df0a4-124">FBadProp</span></span>](fbadprop.md)

