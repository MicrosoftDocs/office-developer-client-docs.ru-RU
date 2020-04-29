---
title: Функция ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Задает аргумент, который может быть передан в пользовательскую функцию, а также значение по умолчанию, возвращаемое пользовательской функцией, если вызывающая ячейка не передает значение аргумента. Возвращает значение, заданное вызывающей ячейкой и сопоставленным параметром Аргнаме.
ms.openlocfilehash: f85c3dc4a49878b034674330f272a63e79c17d49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422728"
---
# <a name="arg-function"></a><span data-ttu-id="625b0-104">Функция ARG</span><span class="sxs-lookup"><span data-stu-id="625b0-104">ARG Function</span></span>

<span data-ttu-id="625b0-105">Задает аргумент, который может быть передан в пользовательскую функцию, а также значение по умолчанию, возвращаемое пользовательской функцией, если вызывающая ячейка не передает значение аргумента.</span><span class="sxs-lookup"><span data-stu-id="625b0-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="625b0-106">Возвращает значение, заданное вызывающей ячейкой и сопоставленным параметром Аргнаме.</span><span class="sxs-lookup"><span data-stu-id="625b0-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="625b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="625b0-107">Syntax</span></span>

<span data-ttu-id="625b0-108">ARG (\* \* *аргнаме* \* *, [* \* *DefaultValue* \* \*])</span><span class="sxs-lookup"><span data-stu-id="625b0-108">ARG(\*\* *argName* \*\*,[ \*\* *defaultValue* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="625b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="625b0-109">Parameters</span></span>

|<span data-ttu-id="625b0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="625b0-110">**Name**</span></span>|<span data-ttu-id="625b0-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="625b0-111">**Required/Optional**</span></span>|<span data-ttu-id="625b0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="625b0-112">**Data Type**</span></span>|<span data-ttu-id="625b0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="625b0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="625b0-114">_аргнаме_</span><span class="sxs-lookup"><span data-stu-id="625b0-114">_argName_</span></span> <br/> |<span data-ttu-id="625b0-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="625b0-115">Required</span></span>  <br/> |<span data-ttu-id="625b0-116">**String**</span><span class="sxs-lookup"><span data-stu-id="625b0-116">**String**</span></span> <br/> |<span data-ttu-id="625b0-117">Имя аргумента, который может быть передан в функцию с помощью вызывающей ячейки.</span><span class="sxs-lookup"><span data-stu-id="625b0-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="625b0-118">_Значение по умолчанию_</span><span class="sxs-lookup"><span data-stu-id="625b0-118">_default Value_</span></span> <br/> |<span data-ttu-id="625b0-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="625b0-119">Optional</span></span>  <br/> |<span data-ttu-id="625b0-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="625b0-120">**Numeric**</span></span> <br/> |<span data-ttu-id="625b0-121">Значение, возвращаемое аргументом ARG, если вызывающая ячейка не передается значение параметра _аргнаме_ .</span><span class="sxs-lookup"><span data-stu-id="625b0-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="625b0-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="625b0-122">Remarks</span></span>

<span data-ttu-id="625b0-123">Разработчик фигуры может создавать пользовательские функции, размещая выражение в одной ячейке и вызывая это выражение из одной или нескольких других ячеек.</span><span class="sxs-lookup"><span data-stu-id="625b0-123">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells.</span></span> <span data-ttu-id="625b0-124">Выражение может содержать строковые литералы, функции таблицы свойств фигуры и ссылки на ячейки.</span><span class="sxs-lookup"><span data-stu-id="625b0-124">The expression can include literal strings, ShapeSheet functions, and cell references.</span></span> <span data-ttu-id="625b0-125">Выражение также может содержать определенные аргументы, передаваемые в вызывающую ячейку.</span><span class="sxs-lookup"><span data-stu-id="625b0-125">The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="625b0-126">В вызывающей ячейке указывается ячейка, содержащая пользовательскую функцию, а также аргументы, которые она хочет передать в функцию.</span><span class="sxs-lookup"><span data-stu-id="625b0-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="625b0-127">Вычисляется ячейка выражения и результат возвращается в вызывающую ячейку.</span><span class="sxs-lookup"><span data-stu-id="625b0-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="625b0-128">Пример</span><span class="sxs-lookup"><span data-stu-id="625b0-128">Example</span></span>

<span data-ttu-id="625b0-129">В приведенном ниже примере показано, как использовать функцию ARG вместе с функцией EVALCELL, чтобы найти среднее значение из набора трех значений.</span><span class="sxs-lookup"><span data-stu-id="625b0-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="625b0-130">В ячейке выражения поместите следующий код, определяющий пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="625b0-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="625b0-131">В вызывающих ячейках поместите следующий код, вызывающий пользовательскую функцию:</span><span class="sxs-lookup"><span data-stu-id="625b0-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


