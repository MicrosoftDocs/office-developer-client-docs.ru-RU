---
title: Функция EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Принимает ссылку на ячейку, которая содержит настраиваемую функцию, а также одну или несколько пар значений имени, чтобы передать настраиваемую функцию в качестве аргументов (необязательно). Возвращает вычисляемый результат настраиваемой функции с учетом указанных аргументов и значений.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418906"
---
# <a name="evalcell-function"></a><span data-ttu-id="ef6ce-104">Функция EVALCELL</span><span class="sxs-lookup"><span data-stu-id="ef6ce-104">EVALCELL Function</span></span>

<span data-ttu-id="ef6ce-105">Принимает ссылку на ячейку, которая содержит настраиваемую функцию, а также одну или несколько пар значений имени, чтобы передать настраиваемую функцию в качестве аргументов (необязательно).</span><span class="sxs-lookup"><span data-stu-id="ef6ce-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="ef6ce-106">Возвращает вычисляемый результат настраиваемой функции с учетом указанных аргументов и значений.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ef6ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef6ce-107">Syntax</span></span>

<span data-ttu-id="ef6ce-108">EVALCELL(\*\* *cellRef* \**,[ \*\* *arg1Name,arg1* \*\* ],[* *arg2Name,arg2* \*\* ],...)</span><span class="sxs-lookup"><span data-stu-id="ef6ce-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ef6ce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef6ce-109">Parameters</span></span>

|<span data-ttu-id="ef6ce-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-110">**Name**</span></span>|<span data-ttu-id="ef6ce-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-111">**Required/Optional**</span></span>|<span data-ttu-id="ef6ce-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-112">**Data Type**</span></span>|<span data-ttu-id="ef6ce-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ef6ce-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="ef6ce-114">_cellRef_</span></span> <br/> |<span data-ttu-id="ef6ce-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ef6ce-115">Required</span></span>  <br/> |<span data-ttu-id="ef6ce-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-116">**String**</span></span> <br/> |<span data-ttu-id="ef6ce-117">Ссылка на ячейку, которая содержит настраиваемую функцию.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="ef6ce-118">Разрешены ссылки на перекрестные листы.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="ef6ce-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="ef6ce-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="ef6ce-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ef6ce-120">Optional</span></span>  <br/> |<span data-ttu-id="ef6ce-121">**String**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-121">**String**</span></span> <br/> |<span data-ttu-id="ef6ce-122">Имя первого аргумента, который будет передан настраиваемой функции.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="ef6ce-123">Разрешены пробелы.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="ef6ce-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="ef6ce-124">_arg1_</span></span> <br/> |<span data-ttu-id="ef6ce-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ef6ce-125">Optional</span></span>  <br/> |<span data-ttu-id="ef6ce-126">**Разные**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-126">**Varies**</span></span> <br/> |<span data-ttu-id="ef6ce-127">Значение _параметра arg1._</span><span class="sxs-lookup"><span data-stu-id="ef6ce-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="ef6ce-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="ef6ce-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="ef6ce-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ef6ce-129">Optional</span></span>  <br/> |<span data-ttu-id="ef6ce-130">**String**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-130">**String**</span></span> <br/> |<span data-ttu-id="ef6ce-131">Имя второго аргумента, который будет передан настраиваемой функции.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="ef6ce-132">Разрешены пробелы.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="ef6ce-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="ef6ce-133">_arg2_</span></span> <br/> |<span data-ttu-id="ef6ce-134">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ef6ce-134">Optional</span></span>  <br/> |<span data-ttu-id="ef6ce-135">**Разные**</span><span class="sxs-lookup"><span data-stu-id="ef6ce-135">**Varies**</span></span> <br/> |<span data-ttu-id="ef6ce-136">Значение _параметра arg2._</span><span class="sxs-lookup"><span data-stu-id="ef6ce-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ef6ce-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef6ce-137">Return value</span></span>

<span data-ttu-id="ef6ce-138">Номер</span><span class="sxs-lookup"><span data-stu-id="ef6ce-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef6ce-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef6ce-139">Remarks</span></span>

<span data-ttu-id="ef6ce-140">Ячейка вызова не должна указывать каждый аргумент, используемый настраиваемой функцией.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ef6ce-141">Пример</span><span class="sxs-lookup"><span data-stu-id="ef6ce-141">Example</span></span>

<span data-ttu-id="ef6ce-142">В следующем примере показано, как использовать функцию EVALCELL совместно с функцией ARG для поиска среднего значения из набора из трех значений.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="ef6ce-143">В ячейке выражения поместите следующий код, определяемый настраиваемой функцией:</span><span class="sxs-lookup"><span data-stu-id="ef6ce-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="ef6ce-144">В ячейках вызова поместите следующий код, который вызывает настраиваемую функцию:</span><span class="sxs-lookup"><span data-stu-id="ef6ce-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


