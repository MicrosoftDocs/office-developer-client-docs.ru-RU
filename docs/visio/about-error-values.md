---
title: Сведения о значениях ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Ошибка значения отображаются в ячейках, которые имеют неправильный формулы для этой ячейки.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813106"
---
# <a name="about-error-values"></a><span data-ttu-id="f3889-103">Сведения о значениях ошибок</span><span class="sxs-lookup"><span data-stu-id="f3889-103">About Error Values</span></span>

<span data-ttu-id="f3889-104">Ошибка значения отображаются в ячейках, которые имеют неправильный формулы для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="f3889-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="f3889-105">Если формула ссылается на ячейку, содержащую значение ошибки, что формулы также отображается значение.</span><span class="sxs-lookup"><span data-stu-id="f3889-105">If a formula references a cell that contains an error value, that formula also displays an error value.</span></span> <span data-ttu-id="f3889-106">Функция ЕОШ, ISERRNA, ЕОШИБКА или ISERRVALUE можно использовать для поиска ошибок.</span><span class="sxs-lookup"><span data-stu-id="f3889-106">You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="f3889-107">**Значения ошибок**</span><span class="sxs-lookup"><span data-stu-id="f3889-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="f3889-108">**Если в ячейке отображается**</span><span class="sxs-lookup"><span data-stu-id="f3889-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="f3889-109">**Содержит формулу**</span><span class="sxs-lookup"><span data-stu-id="f3889-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="f3889-110">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f3889-110">**Example**</span></span> <br/> |
| <span data-ttu-id="f3889-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="f3889-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="f3889-112">Деление на 0</span><span class="sxs-lookup"><span data-stu-id="f3889-112">Division by 0</span></span>  <br/> |<span data-ttu-id="f3889-113">10/0</span><span class="sxs-lookup"><span data-stu-id="f3889-113">10/0</span></span>  <br/> |
| <span data-ttu-id="f3889-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="f3889-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="f3889-115">Аргумент или операнд недопустимого типа</span><span class="sxs-lookup"><span data-stu-id="f3889-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="f3889-116">5 + «Дом»</span><span class="sxs-lookup"><span data-stu-id="f3889-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="f3889-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="f3889-117">#REF!</span></span>  <br/> | <span data-ttu-id="f3889-118">Ссылка на ячейку, не существует</span><span class="sxs-lookup"><span data-stu-id="f3889-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="f3889-119">Ячейки, на который ссылается на ячейку, который больше не существует</span><span class="sxs-lookup"><span data-stu-id="f3889-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="f3889-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="f3889-120">#NUM!</span></span>  <br/> | <span data-ttu-id="f3889-121">Неверный номер</span><span class="sxs-lookup"><span data-stu-id="f3889-121">An invalid number</span></span>  <br/> | <span data-ttu-id="f3889-122">Квадратный корень из отрицательное значение</span><span class="sxs-lookup"><span data-stu-id="f3889-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="f3889-123"># Н/Д!</span><span class="sxs-lookup"><span data-stu-id="f3889-123">#N/A!</span></span>  <br/> | <span data-ttu-id="f3889-124">Не доступное значение</span><span class="sxs-lookup"><span data-stu-id="f3889-124">Not an available value</span></span>  <br/> | <span data-ttu-id="f3889-125">Функция НД)</span><span class="sxs-lookup"><span data-stu-id="f3889-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="f3889-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="f3889-126">#DIM!</span></span>  <br/> | <span data-ttu-id="f3889-127">Измерения значение, превышающее диапазон измерений (допустимый степени являются целые числа от -128 \<= n \<= 127)</span><span class="sxs-lookup"><span data-stu-id="f3889-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="f3889-128">Измерения значение, используемое в неподходящие операции</span><span class="sxs-lookup"><span data-stu-id="f3889-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="f3889-129">1 в ^ 100 \* 1 в ^ 100 (результатом будет 1 в ^ 200, который находится за пределами диапазона аналитики)</span><span class="sxs-lookup"><span data-stu-id="f3889-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="f3889-130">5.2 cm ^ 1,5 (не power целое число)</span><span class="sxs-lookup"><span data-stu-id="f3889-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

