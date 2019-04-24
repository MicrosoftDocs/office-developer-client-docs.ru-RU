---
title: Функция EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Принимает ссылку на ячейку, содержащую настраиваемую функцию, а также одну или несколько пар "имя-значение", которые передаются в пользовательскую функцию в качестве аргументов (необязательно). Возвращает вычисленный результат пользовательской функции с заданными аргументами и значениями.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329073"
---
# <a name="evalcell-function"></a><span data-ttu-id="867d7-104">Функция EVALCELL</span><span class="sxs-lookup"><span data-stu-id="867d7-104">EVALCELL Function</span></span>

<span data-ttu-id="867d7-105">Принимает ссылку на ячейку, содержащую настраиваемую функцию, а также одну или несколько пар "имя-значение", которые передаются в пользовательскую функцию в качестве аргументов (необязательно).</span><span class="sxs-lookup"><span data-stu-id="867d7-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="867d7-106">Возвращает вычисленный результат пользовательской функции с заданными аргументами и значениями.</span><span class="sxs-lookup"><span data-stu-id="867d7-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="867d7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="867d7-107">Syntax</span></span>

<span data-ttu-id="867d7-108">EVALCELL (\* \* *целлреф* \* *, [* \* *arg1Name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="867d7-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="867d7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="867d7-109">Parameters</span></span>

|<span data-ttu-id="867d7-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="867d7-110">**Name**</span></span>|<span data-ttu-id="867d7-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="867d7-111">**Required/Optional**</span></span>|<span data-ttu-id="867d7-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="867d7-112">**Data Type**</span></span>|<span data-ttu-id="867d7-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="867d7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="867d7-114">_Целлреф_</span><span class="sxs-lookup"><span data-stu-id="867d7-114">_cellRef_</span></span> <br/> |<span data-ttu-id="867d7-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="867d7-115">Required</span></span>  <br/> |<span data-ttu-id="867d7-116">**String**</span><span class="sxs-lookup"><span data-stu-id="867d7-116">**String**</span></span> <br/> |<span data-ttu-id="867d7-117">Ссылка на ячейку, содержащую настраиваемую функцию.</span><span class="sxs-lookup"><span data-stu-id="867d7-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="867d7-118">Допускается использование ссылок на несколько страниц.</span><span class="sxs-lookup"><span data-stu-id="867d7-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="867d7-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="867d7-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="867d7-120">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="867d7-120">Optional</span></span>  <br/> |<span data-ttu-id="867d7-121">**String**</span><span class="sxs-lookup"><span data-stu-id="867d7-121">**String**</span></span> <br/> |<span data-ttu-id="867d7-122">Имя первого аргумента, передаваемого в пользовательскую функцию.</span><span class="sxs-lookup"><span data-stu-id="867d7-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="867d7-123">Допускаются пробелы.</span><span class="sxs-lookup"><span data-stu-id="867d7-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="867d7-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="867d7-124">_arg1_</span></span> <br/> |<span data-ttu-id="867d7-125">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="867d7-125">Optional</span></span>  <br/> |<span data-ttu-id="867d7-126">**Разные**</span><span class="sxs-lookup"><span data-stu-id="867d7-126">**Varies**</span></span> <br/> |<span data-ttu-id="867d7-127">Значение параметра _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="867d7-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="867d7-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="867d7-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="867d7-129">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="867d7-129">Optional</span></span>  <br/> |<span data-ttu-id="867d7-130">**String**</span><span class="sxs-lookup"><span data-stu-id="867d7-130">**String**</span></span> <br/> |<span data-ttu-id="867d7-131">Имя второго аргумента, передаваемого в пользовательскую функцию.</span><span class="sxs-lookup"><span data-stu-id="867d7-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="867d7-132">Допускаются пробелы.</span><span class="sxs-lookup"><span data-stu-id="867d7-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="867d7-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="867d7-133">_arg2_</span></span> <br/> |<span data-ttu-id="867d7-134">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="867d7-134">Optional</span></span>  <br/> |<span data-ttu-id="867d7-135">**Разные**</span><span class="sxs-lookup"><span data-stu-id="867d7-135">**Varies**</span></span> <br/> |<span data-ttu-id="867d7-136">Значение параметра _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="867d7-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="867d7-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="867d7-137">Return value</span></span>

<span data-ttu-id="867d7-138">Номер</span><span class="sxs-lookup"><span data-stu-id="867d7-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="867d7-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="867d7-139">Remarks</span></span>

<span data-ttu-id="867d7-140">В вызывающей ячейке не требуется указывать каждый аргумент, используемый пользовательской функцией.</span><span class="sxs-lookup"><span data-stu-id="867d7-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="867d7-141">Пример</span><span class="sxs-lookup"><span data-stu-id="867d7-141">Example</span></span>

<span data-ttu-id="867d7-142">В приведенном ниже примере показано, как с помощью функции EVALCELL в сочетании с АРГУМЕНТом ARG найти среднее значение из набора трех значений.</span><span class="sxs-lookup"><span data-stu-id="867d7-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="867d7-143">В ячейке выражения поместите следующий код, определяющий пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="867d7-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="867d7-144">В вызывающих ячейках поместите следующий код, вызывающий пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="867d7-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


