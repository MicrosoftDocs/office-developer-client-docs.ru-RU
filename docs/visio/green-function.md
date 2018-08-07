---
title: Функция GREEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Возвращает значение зеленого компонента цвета.
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813895"
---
# <a name="green-function"></a><span data-ttu-id="7f4c1-103">Функция GREEN</span><span class="sxs-lookup"><span data-stu-id="7f4c1-103">GREEN Function</span></span>

<span data-ttu-id="7f4c1-104">Возвращает значение зеленого компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7f4c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f4c1-105">Syntax</span></span>

<span data-ttu-id="7f4c1-106">Зеленый (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="7f4c1-106">GREEN(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7f4c1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f4c1-107">Parameters</span></span>

|<span data-ttu-id="7f4c1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7f4c1-108">**Name**</span></span>|<span data-ttu-id="7f4c1-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7f4c1-109">**Required/Optional**</span></span>|<span data-ttu-id="7f4c1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7f4c1-110">**Data Type**</span></span>|<span data-ttu-id="7f4c1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f4c1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7f4c1-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="7f4c1-112">_expression_</span></span> <br/> |<span data-ttu-id="7f4c1-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f4c1-113">Required</span></span>  <br/> |<span data-ttu-id="7f4c1-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="7f4c1-114">**Varies**</span></span> <br/> |<span data-ttu-id="7f4c1-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемые цвета (например, RGB или HSL) или ссылку на ячейку, содержащую цвет индекса или цветовой результатов.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7f4c1-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7f4c1-116">Return value</span></span>

<span data-ttu-id="7f4c1-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="7f4c1-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f4c1-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7f4c1-118">Remarks</span></span>

<span data-ttu-id="7f4c1-119">Возвращаемое значение — это число в диапазоне от 0 до 255 включительно, или ссылка на ячейку, которая разрешается в индекс.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="7f4c1-120">Если *выражение* является недопустимым, он возвращает 0 (черный цвет).</span><span class="sxs-lookup"><span data-stu-id="7f4c1-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7f4c1-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f4c1-121">Example 1</span></span>

<span data-ttu-id="7f4c1-122">Зеленый (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="7f4c1-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="7f4c1-123">Возвращает значение зеленого компонента цвет заливки Sheet. 4.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7f4c1-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7f4c1-124">Example 2</span></span>

<span data-ttu-id="7f4c1-125">GREEN(11)</span><span class="sxs-lookup"><span data-stu-id="7f4c1-125">GREEN(11)</span></span>
  
<span data-ttu-id="7f4c1-126">Возвращает 128, если в документе используется по умолчанию Visio цветовой палитры, в котором темно-желтый цвет по индексу 11.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7f4c1-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7f4c1-127">Example 3</span></span>

<span data-ttu-id="7f4c1-128">ЗЕЛЕНЫЙ (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="7f4c1-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="7f4c1-129">Возвращает 20.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-129">Returns 20.</span></span>
  

