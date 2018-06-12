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
description: Сохраняет значение, заданное через действие пользовательского интерфейса (UI) или автоматизации.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814765"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="ef67d-103">Функция SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="ef67d-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="ef67d-104">Сохраняет значение, заданное через действие пользовательского интерфейса (UI) или автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ef67d-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ef67d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef67d-105">Syntax</span></span>

<span data-ttu-id="ef67d-106">SETATREFEXPR ([** *expr_opt* **])</span><span class="sxs-lookup"><span data-stu-id="ef67d-106">SETATREFEXPR ([ ** *expr_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ef67d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef67d-107">Parameters</span></span>

|<span data-ttu-id="ef67d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ef67d-108">**Name**</span></span>|<span data-ttu-id="ef67d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="ef67d-109">**Required/Optional**</span></span>|<span data-ttu-id="ef67d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ef67d-110">**Data Type**</span></span>|<span data-ttu-id="ef67d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef67d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ef67d-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="ef67d-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="ef67d-113">Optional</span><span class="sxs-lookup"><span data-stu-id="ef67d-113">Optional</span></span>  <br/> |<span data-ttu-id="ef67d-114">**Может отличаться**</span><span class="sxs-lookup"><span data-stu-id="ef67d-114">**Varies**</span></span> <br/> |<span data-ttu-id="ef67d-115">Выражение, которое заменяется значение или выражение, назначаемое для связанной ячейки в ВЫРАЖЕНИЕ_МНОЖЕСТВА функции.</span><span class="sxs-lookup"><span data-stu-id="ef67d-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="ef67d-116">Если не указано, его начальное значение равно 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="ef67d-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef67d-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef67d-117">Remarks</span></span>

<span data-ttu-id="ef67d-118">Значение выражения SETATREFEXPR можно также задать из ВЫРАЖЕНИЕ_МНОЖЕСТВА функции в другую ячейку, которая ссылается на ячейку, содержащий выражение SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="ef67d-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="ef67d-119">Вы не только с помощью функции SETATREFEXPR в качестве параметра ВЫРАЖЕНИЕ_МНОЖЕСТВА функции.</span><span class="sxs-lookup"><span data-stu-id="ef67d-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ef67d-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef67d-120">Example 1</span></span>

<span data-ttu-id="ef67d-121">В следующем примере функция SETATREFEXPR убедитесь, что фигуры по ширине текст.</span><span class="sxs-lookup"><span data-stu-id="ef67d-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="ef67d-122">Ширина =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="ef67d-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ef67d-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ef67d-123">Example 2</span></span>

<span data-ttu-id="ef67d-124">В следующем примере показано, как можно использовать функцию SETATREFEXPR для фигур для привязки к настраиваемой сетке.</span><span class="sxs-lookup"><span data-stu-id="ef67d-124">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid.</span></span> <span data-ttu-id="ef67d-125">Формулы SETATREFEXPR помещаются в ячейках PinX и PinY вызывает ошибку фигуры ПИН-кода для привязки к сетке, определенных в User.GridX и User.GridY.</span><span class="sxs-lookup"><span data-stu-id="ef67d-125">The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="ef67d-126">User.GridX = 2</span><span class="sxs-lookup"><span data-stu-id="ef67d-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="ef67d-127">User.GridY = 2</span><span class="sxs-lookup"><span data-stu-id="ef67d-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="ef67d-128">PinX = INT (SETATREFEXPR /User.GridX () +.5)\*User.GridX</span><span class="sxs-lookup"><span data-stu-id="ef67d-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="ef67d-129">PinY = INT (SETATREFEXPR /User.GridY () +.5)\*User.GridY</span><span class="sxs-lookup"><span data-stu-id="ef67d-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ef67d-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ef67d-130">Example 3</span></span>

<span data-ttu-id="ef67d-131">Пример с помощью функции SETATREFEXPR с ВЫРАЖЕНИЕ_МНОЖЕСТВА функции в разделе [ВЫРАЖЕНИЕ_МНОЖЕСТВА](setatref-function.md) функции.</span><span class="sxs-lookup"><span data-stu-id="ef67d-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

