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
# <a name="about-error-values"></a><span data-ttu-id="d2810-103">О значениях ошибок</span><span class="sxs-lookup"><span data-stu-id="d2810-103">About Error Values</span></span>

<span data-ttu-id="d2810-104">Значения ошибок отображаются в ячейках с неправильными формулами для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="d2810-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="d2810-105">Если формула ссылается на ячейку, содержаную значение ошибки, эта формула также отображает значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="d2810-105">If a formula references a cell that contains an error value, that formula also displays an error value.</span></span> <span data-ttu-id="d2810-106">Для искомые значения ошибок можно использовать функции ISERR, ISERRNA, ISERROR или ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="d2810-106">You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="d2810-107">**Значения ошибок**</span><span class="sxs-lookup"><span data-stu-id="d2810-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="d2810-108">**Если ячейка отображается**</span><span class="sxs-lookup"><span data-stu-id="d2810-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="d2810-109">**Формула включает**</span><span class="sxs-lookup"><span data-stu-id="d2810-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="d2810-110">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d2810-110">**Example**</span></span> <br/> |
| <span data-ttu-id="d2810-111">#ДЕЛ/0!</span><span class="sxs-lookup"><span data-stu-id="d2810-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="d2810-112">Деление на 0</span><span class="sxs-lookup"><span data-stu-id="d2810-112">Division by 0</span></span>  <br/> |<span data-ttu-id="d2810-113">10/0</span><span class="sxs-lookup"><span data-stu-id="d2810-113">10/0</span></span>  <br/> |
| <span data-ttu-id="d2810-114">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="d2810-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="d2810-115">Аргумент или операнд неправильного типа</span><span class="sxs-lookup"><span data-stu-id="d2810-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="d2810-116">5 + "House"</span><span class="sxs-lookup"><span data-stu-id="d2810-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="d2810-117">#ССЫЛКА!</span><span class="sxs-lookup"><span data-stu-id="d2810-117">#REF!</span></span>  <br/> | <span data-ttu-id="d2810-118">Ссылка на ячейку, которая не существует</span><span class="sxs-lookup"><span data-stu-id="d2810-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="d2810-119">Ячейка, которая ссылается на другую ячейку, которая больше не существует</span><span class="sxs-lookup"><span data-stu-id="d2810-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="d2810-120">#ЧИСЛО!</span><span class="sxs-lookup"><span data-stu-id="d2810-120">#NUM!</span></span>  <br/> | <span data-ttu-id="d2810-121">Недопустимый номер</span><span class="sxs-lookup"><span data-stu-id="d2810-121">An invalid number</span></span>  <br/> | <span data-ttu-id="d2810-122">Квадратный корень отрицательного числа</span><span class="sxs-lookup"><span data-stu-id="d2810-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="d2810-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="d2810-123">#N/A!</span></span>  <br/> | <span data-ttu-id="d2810-124">Не доступное значение</span><span class="sxs-lookup"><span data-stu-id="d2810-124">Not an available value</span></span>  <br/> | <span data-ttu-id="d2810-125">Функция NA( )</span><span class="sxs-lookup"><span data-stu-id="d2810-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="d2810-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="d2810-126">#DIM!</span></span>  <br/> | <span data-ttu-id="d2810-127">Значение измерения, превышающая диапазон измерений (допустимые значения: integers -128 \< = n \< = 127)</span><span class="sxs-lookup"><span data-stu-id="d2810-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="d2810-128">Значение измерения, используемое с недопустимой операцией</span><span class="sxs-lookup"><span data-stu-id="d2810-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="d2810-129">1in^100 \* 1in^100 (результат — 1in^200, который выходит за пределы диапазона измерений)</span><span class="sxs-lookup"><span data-stu-id="d2810-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="d2810-130">5.2cm^1.5 (а не мощность в 1,5)</span><span class="sxs-lookup"><span data-stu-id="d2810-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

