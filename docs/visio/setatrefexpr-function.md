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
description: Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="6487e-103">Функция SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="6487e-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="6487e-104">Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6487e-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6487e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6487e-105">Syntax</span></span>

<span data-ttu-id="6487e-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="6487e-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6487e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6487e-107">Parameters</span></span>

|<span data-ttu-id="6487e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6487e-108">**Name**</span></span>|<span data-ttu-id="6487e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6487e-109">**Required/Optional**</span></span>|<span data-ttu-id="6487e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6487e-110">**Data Type**</span></span>|<span data-ttu-id="6487e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6487e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6487e-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="6487e-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="6487e-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="6487e-113">Optional</span></span>  <br/> |<span data-ttu-id="6487e-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="6487e-114">**Varies**</span></span> <br/> |<span data-ttu-id="6487e-115">Выражение, которое заменяется значением или выражением, назначенным со ссылкой на ячейку в функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="6487e-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="6487e-116">Если не указано, его начальное значение — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6487e-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6487e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="6487e-117">Remarks</span></span>

<span data-ttu-id="6487e-118">Значение выражения SETATREFEXPR можно также задать из функции SETATREF в другой ячейке, которая ссылается на ячейку, содержащую выражение SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="6487e-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="6487e-119">Вы не ограничивается использованием функции SETATREFEXPR в качестве параметра функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="6487e-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6487e-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6487e-120">Example 1</span></span>

<span data-ttu-id="6487e-121">В следующем примере используется функция SETATREFEXPR для обеспечения того, чтобы форма была такой же широкой, как и ее текст.</span><span class="sxs-lookup"><span data-stu-id="6487e-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="6487e-122">Width =MAX(TEXTWIDTH(TheText), SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="6487e-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6487e-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6487e-123">Example 2</span></span>

<span data-ttu-id="6487e-124">В следующем примере показано, как можно использовать функцию SETATREFEXPR для привязки фигур к настраиваемой сетке.</span><span class="sxs-lookup"><span data-stu-id="6487e-124">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid.</span></span> <span data-ttu-id="6487e-125">Формулы SETATREFEXPR помещаются в ячейки PinX и PinY, в результате чего пин-код фигуры прикрепляется к сетке, определенной в User.GridX и User.GridY.</span><span class="sxs-lookup"><span data-stu-id="6487e-125">The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="6487e-126">User.GridX =2 in</span><span class="sxs-lookup"><span data-stu-id="6487e-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="6487e-127">User.GridY =2 in</span><span class="sxs-lookup"><span data-stu-id="6487e-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="6487e-128">PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX</span><span class="sxs-lookup"><span data-stu-id="6487e-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="6487e-129">PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY</span><span class="sxs-lookup"><span data-stu-id="6487e-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6487e-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6487e-130">Example 3</span></span>

<span data-ttu-id="6487e-131">Пример использования функции SETATREFEXPR с функцией SETATREF см. в примере [функции SETATREF.](setatref-function.md)</span><span class="sxs-lookup"><span data-stu-id="6487e-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

