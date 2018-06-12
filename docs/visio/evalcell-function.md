---
title: Функция EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Получает ссылку на ячейку, содержащую пользовательскую функцию, а также один или несколько пар имя значение для передачи пользовательской функции аргументов (необязательно). Возвращает вычисляемые результат пользовательской функции указанного аргументов и значения.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813696"
---
# <a name="evalcell-function"></a><span data-ttu-id="9ae62-104">Функция EVALCELL</span><span class="sxs-lookup"><span data-stu-id="9ae62-104">EVALCELL Function</span></span>

<span data-ttu-id="9ae62-105">Получает ссылку на ячейку, содержащую пользовательскую функцию, а также один или несколько пар имя значение для передачи пользовательской функции аргументов (необязательно).</span><span class="sxs-lookup"><span data-stu-id="9ae62-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="9ae62-106">Возвращает вычисляемые результат пользовательской функции указанного аргументов и значения.</span><span class="sxs-lookup"><span data-stu-id="9ae62-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9ae62-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ae62-107">Syntax</span></span>

<span data-ttu-id="9ae62-108">EVALCELL (** *cellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **],...)</span><span class="sxs-lookup"><span data-stu-id="9ae62-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9ae62-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae62-109">Parameters</span></span>

|<span data-ttu-id="9ae62-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9ae62-110">**Name**</span></span>|<span data-ttu-id="9ae62-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="9ae62-111">**Required/Optional**</span></span>|<span data-ttu-id="9ae62-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9ae62-112">**Data Type**</span></span>|<span data-ttu-id="9ae62-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9ae62-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9ae62-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="9ae62-114">_cellRef_</span></span> <br/> |<span data-ttu-id="9ae62-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9ae62-115">Required</span></span>  <br/> |<span data-ttu-id="9ae62-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="9ae62-116">**String**</span></span> <br/> |<span data-ttu-id="9ae62-117">Ссылка на ячейку, содержащую пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="9ae62-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="9ae62-118">Ссылки на разных листах разрешены.</span><span class="sxs-lookup"><span data-stu-id="9ae62-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="9ae62-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="9ae62-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="9ae62-120">Optional</span><span class="sxs-lookup"><span data-stu-id="9ae62-120">Optional</span></span>  <br/> |<span data-ttu-id="9ae62-121">**Строка**</span><span class="sxs-lookup"><span data-stu-id="9ae62-121">**String**</span></span> <br/> |<span data-ttu-id="9ae62-122">Имя первый аргумент будет передан в пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="9ae62-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="9ae62-123">Использовать пробелы.</span><span class="sxs-lookup"><span data-stu-id="9ae62-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="9ae62-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="9ae62-124">_arg1_</span></span> <br/> |<span data-ttu-id="9ae62-125">Optional</span><span class="sxs-lookup"><span data-stu-id="9ae62-125">Optional</span></span>  <br/> |<span data-ttu-id="9ae62-126">**Может отличаться**</span><span class="sxs-lookup"><span data-stu-id="9ae62-126">**Varies**</span></span> <br/> |<span data-ttu-id="9ae62-127">Значение параметра _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="9ae62-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="9ae62-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="9ae62-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="9ae62-129">Optional</span><span class="sxs-lookup"><span data-stu-id="9ae62-129">Optional</span></span>  <br/> |<span data-ttu-id="9ae62-130">**Строка**</span><span class="sxs-lookup"><span data-stu-id="9ae62-130">**String**</span></span> <br/> |<span data-ttu-id="9ae62-131">Имя второй аргумент будет передан в пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="9ae62-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="9ae62-132">Использовать пробелы.</span><span class="sxs-lookup"><span data-stu-id="9ae62-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="9ae62-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="9ae62-133">_arg2_</span></span> <br/> |<span data-ttu-id="9ae62-134">Optional</span><span class="sxs-lookup"><span data-stu-id="9ae62-134">Optional</span></span>  <br/> |<span data-ttu-id="9ae62-135">**Может отличаться**</span><span class="sxs-lookup"><span data-stu-id="9ae62-135">**Varies**</span></span> <br/> |<span data-ttu-id="9ae62-136">Значение параметра _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="9ae62-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9ae62-137">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9ae62-137">Return value</span></span>

<span data-ttu-id="9ae62-138">Число</span><span class="sxs-lookup"><span data-stu-id="9ae62-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ae62-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ae62-139">Remarks</span></span>

<span data-ttu-id="9ae62-140">Вызывающий ячейки не имеет каждый аргумент, используемый в пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="9ae62-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9ae62-141">Пример</span><span class="sxs-lookup"><span data-stu-id="9ae62-141">Example</span></span>

<span data-ttu-id="9ae62-142">Следующем примере показано, как использовать функцию EVALCELL вместе с функцией аргумент для поиска среднее значение из набора три значения.</span><span class="sxs-lookup"><span data-stu-id="9ae62-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="9ae62-143">В ячейке выражения поместите следующий код, который определяет пользовательские функции:</span><span class="sxs-lookup"><span data-stu-id="9ae62-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="9ae62-144">В вызовах ячеек поместите следующий код, вызывающий пользовательские функции:</span><span class="sxs-lookup"><span data-stu-id="9ae62-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


