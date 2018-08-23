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
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576465"
---
# <a name="currency"></a><span data-ttu-id="0d150-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="0d150-103">CURRENCY</span></span>

  
  
<span data-ttu-id="0d150-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d150-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d150-105">Содержит подписанные 64-разрядное целое, представляющее значение типа currency.</span><span class="sxs-lookup"><span data-stu-id="0d150-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d150-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0d150-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d150-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d150-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="0d150-108">Members</span><span class="sxs-lookup"><span data-stu-id="0d150-108">Members</span></span>

 <span data-ttu-id="0d150-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="0d150-109">**Lo**</span></span>
  
> <span data-ttu-id="0d150-110">Младшие 32 разряда к денежному значению.</span><span class="sxs-lookup"><span data-stu-id="0d150-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="0d150-111">**Привет**</span><span class="sxs-lookup"><span data-stu-id="0d150-111">**Hi**</span></span>
  
> <span data-ttu-id="0d150-112">Старшие 32 разряда к денежному значению.</span><span class="sxs-lookup"><span data-stu-id="0d150-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d150-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d150-113">Remarks</span></span>

<span data-ttu-id="0d150-114">Структура **валюты** является масштабируемое целое число представлением десятичного числа с четырех цифр справа от десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="0d150-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="0d150-115">Например хранимое значение 327500 будет рассматриваться как представление денежной суммы 32.7500.</span><span class="sxs-lookup"><span data-stu-id="0d150-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="0d150-116">Структура **CURRENCY** используется для описания свойства типа PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="0d150-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="0d150-117">Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0d150-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d150-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0d150-118">See also</span></span>



[<span data-ttu-id="0d150-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0d150-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0d150-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="0d150-120">MAPI Structures</span></span>](mapi-structures.md)

