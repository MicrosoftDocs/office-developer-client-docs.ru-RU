---
title: Функция RED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Возвращает красный компонент цвета.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415525"
---
# <a name="red-function"></a><span data-ttu-id="f460a-103">Функция RED</span><span class="sxs-lookup"><span data-stu-id="f460a-103">RED Function</span></span>

<span data-ttu-id="f460a-104">Возвращает красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="f460a-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f460a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f460a-105">Syntax</span></span>

<span data-ttu-id="f460a-106">RED (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f460a-106">RED(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f460a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f460a-107">Parameters</span></span>

|<span data-ttu-id="f460a-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f460a-108">**Name**</span></span>|<span data-ttu-id="f460a-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f460a-109">**Required/Optional**</span></span>|<span data-ttu-id="f460a-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f460a-110">**Data Type**</span></span>|<span data-ttu-id="f460a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f460a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f460a-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="f460a-112">_expression_</span></span> <br/> |<span data-ttu-id="f460a-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f460a-113">Required</span></span>  <br/> |<span data-ttu-id="f460a-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="f460a-114">**Varies**</span></span> <br/> |<span data-ttu-id="f460a-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="f460a-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f460a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f460a-116">Return value</span></span>

<span data-ttu-id="f460a-117">Номер</span><span class="sxs-lookup"><span data-stu-id="f460a-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f460a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f460a-118">Remarks</span></span>

<span data-ttu-id="f460a-119">Возвращаемое значение — число в диапазоне от 0 до 255 включительно, или ссылку на ячейку, которая разрешается в индекс.</span><span class="sxs-lookup"><span data-stu-id="f460a-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="f460a-120">Если _выражение_ недопустимо, эта функция возвращает значение 0 (Black).</span><span class="sxs-lookup"><span data-stu-id="f460a-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f460a-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f460a-121">Example 1</span></span>

<span data-ttu-id="f460a-122">КРАСНЫЙ (22)</span><span class="sxs-lookup"><span data-stu-id="f460a-122">RED(22)</span></span>
  
<span data-ttu-id="f460a-123">Возвращает 51, если в документе используется цветовая палитра Microsoft Office Visio по умолчанию, где темно-серый — цвет с индексом 22.</span><span class="sxs-lookup"><span data-stu-id="f460a-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f460a-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f460a-124">Example 2</span></span>

<span data-ttu-id="f460a-125">КРАСНЫЙ (char. Color)</span><span class="sxs-lookup"><span data-stu-id="f460a-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="f460a-126">Возвращает значение красного компонента текущего цвета шрифта.</span><span class="sxs-lookup"><span data-stu-id="f460a-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f460a-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f460a-127">Example 3</span></span>

<span data-ttu-id="f460a-128">RED (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="f460a-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="f460a-129">Возвращает 10.</span><span class="sxs-lookup"><span data-stu-id="f460a-129">Returns 10.</span></span>
  

