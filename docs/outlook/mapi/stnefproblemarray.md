---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812412"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="13efd-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="13efd-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="13efd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13efd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13efd-105">Содержит массив структур **STnefProblem** , описывающие один или несколько обработки ошибок, возникших во время кодирования или декодирования потока транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="13efd-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13efd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="13efd-106">Header file:</span></span>  <br/> |<span data-ttu-id="13efd-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="13efd-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="13efd-108">Members</span><span class="sxs-lookup"><span data-stu-id="13efd-108">Members</span></span>

 <span data-ttu-id="13efd-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="13efd-109">**cProblem**</span></span>
  
> <span data-ttu-id="13efd-110">Число элементов массива, указанных в элемент **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="13efd-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="13efd-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="13efd-111">**aProblem**</span></span>
  
> <span data-ttu-id="13efd-112">Массив структур [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="13efd-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="13efd-113">Каждая структура содержит сведения о свойства или атрибута обработки проблемы.</span><span class="sxs-lookup"><span data-stu-id="13efd-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="13efd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="13efd-114">Remarks</span></span>

<span data-ttu-id="13efd-115">Если проблема возникает во время обработки свойства или атрибута, выходного параметра в метод [ITnef::ExtractProps](itnef-extractprops.md) и метод [ITnef::Finish](itnef-finish.md) каждого получать указатель на структуру **STnefProblemArray** и **ExtractProps **и **завершить** каждого возвращаемое значение MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="13efd-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="13efd-116">Это значение ошибка указывает, что проблема заданных во время обработки и структуру **STnefProblemArray** был создан.</span><span class="sxs-lookup"><span data-stu-id="13efd-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="13efd-117">Если структуру **STnefProblem** не создан во время обработки атрибут или свойство, клиентское приложение может продолжать в разделе предполагается, что обработка атрибут или свойство успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="13efd-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="13efd-118">Единственное исключение происходит, когда проблемы заданных во время декодирование инкапсуляция блока.</span><span class="sxs-lookup"><span data-stu-id="13efd-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="13efd-119">Если ошибка во время этого декодирования MAPI_E_UNABLE_TO_COMPLETE можно получить как [SCODE](scode.md) в структуре.</span><span class="sxs-lookup"><span data-stu-id="13efd-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="13efd-120">В этом случае декодирования компонента, соответствующего блока остановлена и декодирования располагается в другой компонент.</span><span class="sxs-lookup"><span data-stu-id="13efd-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13efd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="13efd-121">See also</span></span>



[<span data-ttu-id="13efd-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="13efd-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="13efd-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="13efd-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="13efd-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="13efd-124">MAPI Structures</span></span>](mapi-structures.md)

