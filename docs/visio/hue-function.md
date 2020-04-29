---
title: Функция HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Возвращает значение компонента оттенка цвета.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439494"
---
# <a name="hue-function"></a><span data-ttu-id="bf87e-103">Функция HUE</span><span class="sxs-lookup"><span data-stu-id="bf87e-103">HUE Function</span></span>

<span data-ttu-id="bf87e-104">Возвращает значение компонента оттенка цвета.</span><span class="sxs-lookup"><span data-stu-id="bf87e-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bf87e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf87e-105">Syntax</span></span>

<span data-ttu-id="bf87e-106">Оттенок (\* \* *выражение* \* \*)</span><span class="sxs-lookup"><span data-stu-id="bf87e-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bf87e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf87e-107">Parameters</span></span>

|<span data-ttu-id="bf87e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bf87e-108">**Name**</span></span>|<span data-ttu-id="bf87e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="bf87e-109">**Required/Optional**</span></span>|<span data-ttu-id="bf87e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bf87e-110">**Data Type**</span></span>|<span data-ttu-id="bf87e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf87e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bf87e-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="bf87e-112">_expression_</span></span> <br/> |<span data-ttu-id="bf87e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf87e-113">Required</span></span>  <br/> |<span data-ttu-id="bf87e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bf87e-114">**String**</span></span> <br/> |<span data-ttu-id="bf87e-115">Выражение, которое оценивается как цвет.</span><span class="sxs-lookup"><span data-stu-id="bf87e-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bf87e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf87e-116">Return value</span></span>

<span data-ttu-id="bf87e-117">Номер</span><span class="sxs-lookup"><span data-stu-id="bf87e-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf87e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf87e-118">Remarks</span></span>

<span data-ttu-id="bf87e-119">Возвращаемое значение — число в диапазоне от 0 до 239 включительно.</span><span class="sxs-lookup"><span data-stu-id="bf87e-119">The return value is a number in the range 0 to 239, inclusive.</span></span> <span data-ttu-id="bf87e-120">Вход — это индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="bf87e-120">The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span> <span data-ttu-id="bf87e-121">Функция возвращает значение 0 для недопустимых входных данных.</span><span class="sxs-lookup"><span data-stu-id="bf87e-121">The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bf87e-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf87e-122">Example 1</span></span>

<span data-ttu-id="bf87e-123">Оттенок (лист. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="bf87e-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="bf87e-124">Возвращает оттенок цвета переднего плана листа. 4's.</span><span class="sxs-lookup"><span data-stu-id="bf87e-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bf87e-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bf87e-125">Example 2</span></span>

<span data-ttu-id="bf87e-126">ОТТЕНОК (7)</span><span class="sxs-lookup"><span data-stu-id="bf87e-126">HUE(7)</span></span>
  
<span data-ttu-id="bf87e-127">Возвращает 120, если в документе используется цветовая палитра Microsoft Visio по умолчанию, где голубой — цвет с индексом 7.</span><span class="sxs-lookup"><span data-stu-id="bf87e-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bf87e-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bf87e-128">Example 3</span></span>

<span data-ttu-id="bf87e-129">ОТТЕНОК (HSL (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="bf87e-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="bf87e-130">Возвращает 10.</span><span class="sxs-lookup"><span data-stu-id="bf87e-130">Returns 10.</span></span>
  

