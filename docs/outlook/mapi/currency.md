---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431122"
---
# <a name="currency"></a><span data-ttu-id="a9520-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a9520-103">CURRENCY</span></span>

  
  
<span data-ttu-id="a9520-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9520-105">Содержит подписанное 64-битное значение, представляющее значение валюты.</span><span class="sxs-lookup"><span data-stu-id="a9520-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9520-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a9520-106">Header file:</span></span>  <br/> |<span data-ttu-id="a9520-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9520-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="a9520-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a9520-108">Members</span></span>

 <span data-ttu-id="a9520-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="a9520-109">**Lo**</span></span>
  
> <span data-ttu-id="a9520-110">32 бита валюты низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="a9520-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="a9520-111">**Привет**</span><span class="sxs-lookup"><span data-stu-id="a9520-111">**Hi**</span></span>
  
> <span data-ttu-id="a9520-112">32 бита валюты в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="a9520-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9520-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9520-113">Remarks</span></span>

<span data-ttu-id="a9520-114">Структура **CURRENCY** — это масштабное integer-представление десятичной цифры с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="a9520-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="a9520-115">Например, сохраненное значение 327500 следует представить как значение валюты 32,7500.</span><span class="sxs-lookup"><span data-stu-id="a9520-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="a9520-116">Структура **CURRENCY** используется для описания свойства типа PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="a9520-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="a9520-117">Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a9520-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9520-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a9520-118">See also</span></span>



[<span data-ttu-id="a9520-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a9520-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a9520-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a9520-120">MAPI Structures</span></span>](mapi-structures.md)

