---
title: Функция ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Задает аргумент, вызывающую ячейку можно передать в пользовательской функции, а также по умолчанию значение, возвращаемое пользовательской функции Если вызывающая ячейка не передает значение для аргумента. Возвращает значение, заданное вызывающей ячейкой и соответствующим параметром argName.
ms.openlocfilehash: 3d0e126e0fa075ff2a07773197c1973e6b0249d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813182"
---
# <a name="arg-function"></a><span data-ttu-id="cc896-104">Функция ARG</span><span class="sxs-lookup"><span data-stu-id="cc896-104">ARG Function</span></span>

<span data-ttu-id="cc896-105">Задает аргумент, вызывающую ячейку можно передать в пользовательской функции, а также по умолчанию значение, возвращаемое пользовательской функции Если вызывающая ячейка не передает значение для аргумента.</span><span class="sxs-lookup"><span data-stu-id="cc896-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="cc896-106">Возвращает значение, заданное вызывающей ячейкой и соответствующим параметром argName.</span><span class="sxs-lookup"><span data-stu-id="cc896-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cc896-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc896-107">Syntax</span></span>

<span data-ttu-id="cc896-108">Аргумент (** *argName* **, [** *defaultValue* **])</span><span class="sxs-lookup"><span data-stu-id="cc896-108">ARG(** *argName* **,[ ** *defaultValue* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cc896-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc896-109">Parameters</span></span>

|<span data-ttu-id="cc896-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cc896-110">**Name**</span></span>|<span data-ttu-id="cc896-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="cc896-111">**Required/Optional**</span></span>|<span data-ttu-id="cc896-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cc896-112">**Data Type**</span></span>|<span data-ttu-id="cc896-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cc896-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cc896-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="cc896-114">_argName_</span></span> <br/> |<span data-ttu-id="cc896-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cc896-115">Required</span></span>  <br/> |<span data-ttu-id="cc896-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="cc896-116">**String**</span></span> <br/> |<span data-ttu-id="cc896-117">Имя аргумента, вызывающую ячейку можно передать в функцию.</span><span class="sxs-lookup"><span data-stu-id="cc896-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="cc896-118">_Значение по умолчанию_</span><span class="sxs-lookup"><span data-stu-id="cc896-118">_default Value_</span></span> <br/> |<span data-ttu-id="cc896-119">Optional</span><span class="sxs-lookup"><span data-stu-id="cc896-119">Optional</span></span>  <br/> |<span data-ttu-id="cc896-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="cc896-120">**Numeric**</span></span> <br/> |<span data-ttu-id="cc896-121">Значение, возвращенное аргумент, если вызывающий ячейки, не был передан в значение для параметра _argName_ .</span><span class="sxs-lookup"><span data-stu-id="cc896-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc896-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="cc896-122">Remarks</span></span>

<span data-ttu-id="cc896-123">Являясь разработчиком фигуры можно создать пользовательские функции, поместив выражение в одну ячейку и вызов выражения из одной или нескольких секций.</span><span class="sxs-lookup"><span data-stu-id="cc896-123">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells.</span></span> <span data-ttu-id="cc896-124">Выражение может включать буквенные строки, ShapeSheet функции и ссылки на ячейки.</span><span class="sxs-lookup"><span data-stu-id="cc896-124">The expression can include literal strings, ShapeSheet functions, and cell references.</span></span> <span data-ttu-id="cc896-125">Выражение также может включать определенных аргументов, передаваемых в путем вызова ячейки.</span><span class="sxs-lookup"><span data-stu-id="cc896-125">The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="cc896-126">Вызывающий ячейки определяет ячейку с текстом пользовательской функции, а также аргументы, которые требуется передать в функцию.</span><span class="sxs-lookup"><span data-stu-id="cc896-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="cc896-127">Ячейка выражение вычисляется и возвращается результат в вызывающую ячейку.</span><span class="sxs-lookup"><span data-stu-id="cc896-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="cc896-128">Пример</span><span class="sxs-lookup"><span data-stu-id="cc896-128">Example</span></span>

<span data-ttu-id="cc896-129">Следующем примере показано, как использовать функцию аргумент вместе с функцией EVALCELL поиск среднего значения из набора три значения.</span><span class="sxs-lookup"><span data-stu-id="cc896-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="cc896-130">В ячейке выражения поместите следующий код, который определяет пользовательские функции:</span><span class="sxs-lookup"><span data-stu-id="cc896-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="cc896-131">В вызовах ячеек поместите следующий код, вызывающий пользовательские функции:</span><span class="sxs-lookup"><span data-stu-id="cc896-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


