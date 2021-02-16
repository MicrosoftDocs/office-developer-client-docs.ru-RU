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
description: Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="4a3f0-103">Функция SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="4a3f0-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="4a3f0-104">Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе или автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a3f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a3f0-105">Syntax</span></span>

<span data-ttu-id="4a3f0-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="4a3f0-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a3f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a3f0-107">Parameters</span></span>

|<span data-ttu-id="4a3f0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4a3f0-108">**Name**</span></span>|<span data-ttu-id="4a3f0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4a3f0-109">**Required/Optional**</span></span>|<span data-ttu-id="4a3f0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4a3f0-110">**Data Type**</span></span>|<span data-ttu-id="4a3f0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a3f0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a3f0-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="4a3f0-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="4a3f0-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="4a3f0-113">Optional</span></span>  <br/> |<span data-ttu-id="4a3f0-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="4a3f0-114">**Varies**</span></span> <br/> |<span data-ttu-id="4a3f0-115">Выражение, которое заменяется значением или выражением, присвоенным ячейке, на которую ссылается функция SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="4a3f0-116">Если значение не указано, начальное значение — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="4a3f0-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a3f0-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a3f0-117">Remarks</span></span>

<span data-ttu-id="4a3f0-118">Значение выражения SETATREFEXPR также можно установить из функции SETATREF в другой ячейке, которая ссылается на ячейку, содержащую выражение SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="4a3f0-119">В качестве параметра функции SETATREFEXPR можно использовать не только функцию SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4a3f0-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a3f0-120">Example 1</span></span>

<span data-ttu-id="4a3f0-121">В следующем примере функция SETATREFEXPR используется для обеспечения ширины фигуры до ее текста.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="4a3f0-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="4a3f0-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4a3f0-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4a3f0-123">Example 2</span></span>

<span data-ttu-id="4a3f0-124">В следующем примере показано, как можно использовать функцию SETATREFEXPR для привязки фигур к настраиваемой сетке.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-124">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid.</span></span> <span data-ttu-id="4a3f0-125">Формулы SETATREFEXPR помещаются в ячейки PinX и PinY, в результате чего контакт фигуры прикреплен к сетке, определенной в User.GridX и User.GridY.</span><span class="sxs-lookup"><span data-stu-id="4a3f0-125">The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="4a3f0-126">User.GridX =2 in</span><span class="sxs-lookup"><span data-stu-id="4a3f0-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="4a3f0-127">User.GridY =2 in</span><span class="sxs-lookup"><span data-stu-id="4a3f0-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="4a3f0-128">PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX</span><span class="sxs-lookup"><span data-stu-id="4a3f0-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="4a3f0-129">PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY</span><span class="sxs-lookup"><span data-stu-id="4a3f0-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4a3f0-130">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4a3f0-130">Example 3</span></span>

<span data-ttu-id="4a3f0-131">Пример использования функции SETATREFEXPR с функцией SETATREF см. в [функции SETATREF.](setatref-function.md)</span><span class="sxs-lookup"><span data-stu-id="4a3f0-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

