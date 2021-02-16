---
title: Функция ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Указывает аргумент, который вызываемая ячейка может передать настраиваемой функции, а также значение по умолчанию, возвращаемого настраиваемой функцией, если вызываемая ячейка не передает значение аргумента. Возвращает значение, указанное в вызываемой ячейке, и совпадающий параметр argName.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293487"
---
# <a name="arg-function"></a><span data-ttu-id="5e909-104">Функция ARG</span><span class="sxs-lookup"><span data-stu-id="5e909-104">ARG Function</span></span>

<span data-ttu-id="5e909-105">Указывает аргумент, который вызываемая ячейка может передать настраиваемой функции, а также значение по умолчанию, возвращаемого настраиваемой функцией, если вызываемая ячейка не передает значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="5e909-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="5e909-106">Возвращает значение, указанное в вызываемой ячейке, и совпадающий параметр argName.</span><span class="sxs-lookup"><span data-stu-id="5e909-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5e909-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e909-107">Syntax</span></span>

<span data-ttu-id="5e909-108">ARG(***argName***,[ ***defaultValue*** ])</span><span class="sxs-lookup"><span data-stu-id="5e909-108">ARG(***argName***,[ ***defaultValue*** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5e909-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e909-109">Parameters</span></span>

|<span data-ttu-id="5e909-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5e909-110">**Name**</span></span>|<span data-ttu-id="5e909-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5e909-111">**Required/Optional**</span></span>|<span data-ttu-id="5e909-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5e909-112">**Data Type**</span></span>|<span data-ttu-id="5e909-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5e909-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5e909-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="5e909-114">_argName_</span></span> <br/> |<span data-ttu-id="5e909-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5e909-115">Required</span></span>  <br/> |<span data-ttu-id="5e909-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="5e909-116">**String**</span></span> <br/> |<span data-ttu-id="5e909-117">Имя аргумента, который вызываемая ячейка может передать в функцию.</span><span class="sxs-lookup"><span data-stu-id="5e909-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="5e909-118">_значение по умолчанию_</span><span class="sxs-lookup"><span data-stu-id="5e909-118">_default Value_</span></span> <br/> |<span data-ttu-id="5e909-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="5e909-119">Optional</span></span>  <br/> |<span data-ttu-id="5e909-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="5e909-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5e909-121">Значение, возвращаемого ARG, если вызываемая ячейка не передала значение параметра _argName._</span><span class="sxs-lookup"><span data-stu-id="5e909-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e909-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e909-122">Remarks</span></span>

<span data-ttu-id="5e909-123">Разработчик фигуры может создавать пользовательские функции, размещая выражение в одной ячейке и вызывая это выражение из одной или более других ячеек.</span><span class="sxs-lookup"><span data-stu-id="5e909-123">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells.</span></span> <span data-ttu-id="5e909-124">Выражение может включать строки литералов, функции ShapeSheet и ссылки на ячейки.</span><span class="sxs-lookup"><span data-stu-id="5e909-124">The expression can include literal strings, ShapeSheet functions, and cell references.</span></span> <span data-ttu-id="5e909-125">Выражение также может включать определенные аргументы, которые передаются вызываемой ячейкой.</span><span class="sxs-lookup"><span data-stu-id="5e909-125">The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="5e909-126">Вызываемая ячейка указывает ячейку, которая содержит пользовательскую функцию, а также любые аргументы, которые она хочет передать функции.</span><span class="sxs-lookup"><span data-stu-id="5e909-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="5e909-127">Ячейка выражения вычисляется, а результат возвращается вызываемой ячейке.</span><span class="sxs-lookup"><span data-stu-id="5e909-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="5e909-128">Пример</span><span class="sxs-lookup"><span data-stu-id="5e909-128">Example</span></span>

<span data-ttu-id="5e909-129">В следующем примере показано, как использовать функцию ARG в сочетании с функцией EVALCELL для поиска среднего значения из набора из трех значений.</span><span class="sxs-lookup"><span data-stu-id="5e909-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="5e909-130">В ячейке выражения раз поместите следующий код, который определяет пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="5e909-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="5e909-131">В ячейках вызова раз поместите следующий код, который вызывает пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="5e909-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


