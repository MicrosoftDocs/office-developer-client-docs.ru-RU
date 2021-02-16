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
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434265"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="72826-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="72826-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="72826-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72826-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72826-105">Содержит массив структур **STnefProblem,** описывающий одну или несколько проблем обработки, которые произошли во время кодировки или декодирования потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="72826-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72826-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="72826-106">Header file:</span></span>  <br/> |<span data-ttu-id="72826-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="72826-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="72826-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="72826-108">Members</span></span>

 <span data-ttu-id="72826-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="72826-109">**cProblem**</span></span>
  
> <span data-ttu-id="72826-110">Количество элементов в массиве, указанном **в элементе aProblem.**</span><span class="sxs-lookup"><span data-stu-id="72826-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="72826-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="72826-111">**aProblem**</span></span>
  
> <span data-ttu-id="72826-112">Массив [структур STnefProblem.](stnefproblem.md)</span><span class="sxs-lookup"><span data-stu-id="72826-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="72826-113">Каждая структура содержит сведения о проблеме обработки свойств или атрибутов.</span><span class="sxs-lookup"><span data-stu-id="72826-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72826-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="72826-114">Remarks</span></span>

<span data-ttu-id="72826-115">Если во время обработки атрибута или свойства возникает проблема, выходной параметр в методе [ITnef::ExtractProps](itnef-extractprops.md) и в методе [ITnef::Finish](itnef-finish.md) получает указатель на структуру **STnefProblemArray** и **ExtractProps** и finish возвращает значение MAPI_W_ERRORS_RETURNED. </span><span class="sxs-lookup"><span data-stu-id="72826-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="72826-116">Это значение ошибки указывает, что во время обработки возникла проблема и была сформирована структура **STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="72826-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="72826-117">Если структура **STnefProblem** не создается во время обработки атрибута или свойства, клиентские приложения могут продолжить при предположении, что обработка этого атрибута или свойства была успешной.</span><span class="sxs-lookup"><span data-stu-id="72826-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="72826-118">Единственное исключение возникает, когда проблема возникает во время декодирования блока инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="72826-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="72826-119">Если ошибка произошла во время декодирования, MAPI_E_UNABLE_TO_COMPLETE может быть возвращен в качестве [SCODE](scode.md) в структуре.</span><span class="sxs-lookup"><span data-stu-id="72826-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="72826-120">В этом случае декодинг компонента, соответствующего блоку, останавливается, а декодирования продолжается в другом компоненте.</span><span class="sxs-lookup"><span data-stu-id="72826-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72826-121">См. также</span><span class="sxs-lookup"><span data-stu-id="72826-121">See also</span></span>



[<span data-ttu-id="72826-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="72826-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="72826-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="72826-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="72826-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="72826-124">MAPI Structures</span></span>](mapi-structures.md)

