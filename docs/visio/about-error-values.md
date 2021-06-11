---
title: О значениях ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Значения ошибок отображаются в ячейках с неправильными формулами для этой ячейки.
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423869"
---
# <a name="about-error-values"></a><span data-ttu-id="21597-103">О значениях ошибок</span><span class="sxs-lookup"><span data-stu-id="21597-103">About Error Values</span></span>

<span data-ttu-id="21597-104">Значения ошибок отображаются в ячейках с неправильными формулами для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="21597-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="21597-105">Если формула ссылается на ячейку, содержаную значение ошибки, эта формула также отображает значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="21597-105">If a formula references a cell that contains an error value, that formula also displays an error value.</span></span> <span data-ttu-id="21597-106">Чтобы найти значения ошибок, можно использовать функции ISERR, ISERRNA, ISERROR или ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="21597-106">You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="21597-107">**Значения ошибок**</span><span class="sxs-lookup"><span data-stu-id="21597-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="21597-108">**Если ячейка отображает**</span><span class="sxs-lookup"><span data-stu-id="21597-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="21597-109">**Формула включает в себя**</span><span class="sxs-lookup"><span data-stu-id="21597-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="21597-110">**Пример**</span><span class="sxs-lookup"><span data-stu-id="21597-110">**Example**</span></span> <br/> |
| <span data-ttu-id="21597-111">#ДЕЛ/0!</span><span class="sxs-lookup"><span data-stu-id="21597-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="21597-112">Разделение на 0</span><span class="sxs-lookup"><span data-stu-id="21597-112">Division by 0</span></span>  <br/> |<span data-ttu-id="21597-113">10/0</span><span class="sxs-lookup"><span data-stu-id="21597-113">10/0</span></span>  <br/> |
| <span data-ttu-id="21597-114">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="21597-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="21597-115">Аргумент или операнд неправильного типа</span><span class="sxs-lookup"><span data-stu-id="21597-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="21597-116">5 + "Дом"</span><span class="sxs-lookup"><span data-stu-id="21597-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="21597-117">#ССЫЛКА!</span><span class="sxs-lookup"><span data-stu-id="21597-117">#REF!</span></span>  <br/> | <span data-ttu-id="21597-118">Ссылка на ячейку, которая не существует</span><span class="sxs-lookup"><span data-stu-id="21597-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="21597-119">Ячейка, которая ссылается на другую ячейку, которая больше не существует</span><span class="sxs-lookup"><span data-stu-id="21597-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="21597-120">#ЧИСЛО!</span><span class="sxs-lookup"><span data-stu-id="21597-120">#NUM!</span></span>  <br/> | <span data-ttu-id="21597-121">Недействительный номер</span><span class="sxs-lookup"><span data-stu-id="21597-121">An invalid number</span></span>  <br/> | <span data-ttu-id="21597-122">Квадратный корневой корень отрицательного числа</span><span class="sxs-lookup"><span data-stu-id="21597-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="21597-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="21597-123">#N/A!</span></span>  <br/> | <span data-ttu-id="21597-124">Не доступное значение</span><span class="sxs-lookup"><span data-stu-id="21597-124">Not an available value</span></span>  <br/> | <span data-ttu-id="21597-125">ФУНКЦИЯ NA()</span><span class="sxs-lookup"><span data-stu-id="21597-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="21597-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="21597-126">#DIM!</span></span>  <br/> | <span data-ttu-id="21597-127">Размерное значение, которое превышает диапазон измерений (допустимые силы — это ряды -128 \< = n \< = 127)</span><span class="sxs-lookup"><span data-stu-id="21597-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="21597-128">Размерное значение, используемое при ненадлежащей операции</span><span class="sxs-lookup"><span data-stu-id="21597-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="21597-129">1in^100 \* 1in^100 (результат 1in^200, который находится за пределами диапазона измерений)</span><span class="sxs-lookup"><span data-stu-id="21597-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="21597-130">5.2cm^1.5 (не вменая мощность)</span><span class="sxs-lookup"><span data-stu-id="21597-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

