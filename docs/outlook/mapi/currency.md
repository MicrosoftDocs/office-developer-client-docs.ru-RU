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
# <a name="currency"></a><span data-ttu-id="2204b-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2204b-103">CURRENCY</span></span>

  
  
<span data-ttu-id="2204b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2204b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2204b-105">Содержит подписанное 64 — разрядное целое число, представляющее значение денежной единицы.</span><span class="sxs-lookup"><span data-stu-id="2204b-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2204b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2204b-106">Header file:</span></span>  <br/> |<span data-ttu-id="2204b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2204b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="2204b-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="2204b-108">Members</span></span>

 <span data-ttu-id="2204b-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="2204b-109">**Lo**</span></span>
  
> <span data-ttu-id="2204b-110">Младшие биты 32 значения денежной единицы.</span><span class="sxs-lookup"><span data-stu-id="2204b-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="2204b-111">**Привет**</span><span class="sxs-lookup"><span data-stu-id="2204b-111">**Hi**</span></span>
  
> <span data-ttu-id="2204b-112">32 бит высокого порядка для денежного значения.</span><span class="sxs-lookup"><span data-stu-id="2204b-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2204b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="2204b-113">Remarks</span></span>

<span data-ttu-id="2204b-114">Структура **валюты** — это масштабированное целое число десятичного числа с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="2204b-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="2204b-115">Например, сохраненное значение 327500 — это представление денежного значения 32,7500.</span><span class="sxs-lookup"><span data-stu-id="2204b-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="2204b-116">Структура **валюты** используется для описания свойства типа PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="2204b-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="2204b-117">Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2204b-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2204b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2204b-118">See also</span></span>



[<span data-ttu-id="2204b-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2204b-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2204b-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="2204b-120">MAPI Structures</span></span>](mapi-structures.md)

