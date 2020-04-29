---
title: Функция SETATREFEXPR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Сохраняет значение, заданное с помощью действия в пользовательском интерфейсе или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="c1201-103">Функция SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="c1201-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="c1201-104">Сохраняет значение, заданное с помощью действия в пользовательском интерфейсе или автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c1201-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c1201-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1201-105">Syntax</span></span>

<span data-ttu-id="c1201-106">SETATREFEXPR ([\* \* *expr_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="c1201-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c1201-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1201-107">Parameters</span></span>

|<span data-ttu-id="c1201-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c1201-108">**Name**</span></span>|<span data-ttu-id="c1201-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c1201-109">**Required/Optional**</span></span>|<span data-ttu-id="c1201-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c1201-110">**Data Type**</span></span>|<span data-ttu-id="c1201-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1201-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c1201-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="c1201-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="c1201-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="c1201-113">Optional</span></span>  <br/> |<span data-ttu-id="c1201-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="c1201-114">**Varies**</span></span> <br/> |<span data-ttu-id="c1201-115">Выражение, которое заменяется значением или выражением, присваиваемым указанной ячейке в функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="c1201-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="c1201-116">Если не указано, его начальное значение равно 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="c1201-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1201-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1201-117">Remarks</span></span>

<span data-ttu-id="c1201-118">Значение выражения SETATREFEXPR также можно задать из функции SETATREF в другой ячейке, ссылающейся на ячейку, содержащую выражение SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="c1201-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="c1201-119">Использование функции SETATREFEXPR в качестве параметра функции SETATREF не ограничено.</span><span class="sxs-lookup"><span data-stu-id="c1201-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c1201-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1201-120">Example 1</span></span>

<span data-ttu-id="c1201-121">В приведенном ниже примере используется функция SETATREFEXPR, чтобы убедиться, что фигура имеет ширину текста.</span><span class="sxs-lookup"><span data-stu-id="c1201-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="c1201-122">Width = MAX (TEXTWIDTH (TheText), SETATREFEXPR ())</span><span class="sxs-lookup"><span data-stu-id="c1201-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c1201-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c1201-123">Example 2</span></span>

<span data-ttu-id="c1201-124">В приведенном ниже примере показано, как можно использовать функцию SETATREFEXPR, чтобы фигуры привязываются к настраиваемой сетке.</span><span class="sxs-lookup"><span data-stu-id="c1201-124">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid.</span></span> <span data-ttu-id="c1201-125">Формулы SETATREFEXPR размещаются в ячейках PinX и PinY, что приводит к привязке ПИН-кода фигуры к сетке, определенной в файле user. Гридкс и User. Grid.</span><span class="sxs-lookup"><span data-stu-id="c1201-125">The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="c1201-126">User. Гридкс = 2 in</span><span class="sxs-lookup"><span data-stu-id="c1201-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="c1201-127">User. Grid = 2 в</span><span class="sxs-lookup"><span data-stu-id="c1201-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="c1201-128">PinX = INT (SETATREFEXPR ()/Усер.гридкс + 0,5)\*User. гридкс</span><span class="sxs-lookup"><span data-stu-id="c1201-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="c1201-129">PinY = INT (SETATREFEXPR ()/Усер.Гриди + 0,5)\*User. Grid</span><span class="sxs-lookup"><span data-stu-id="c1201-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c1201-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c1201-130">Example 3</span></span>

<span data-ttu-id="c1201-131">Пример использования функции SETATREFEXPR с функцией SETATREF представлен в разделе Функция [SETATREF](setatref-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c1201-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

