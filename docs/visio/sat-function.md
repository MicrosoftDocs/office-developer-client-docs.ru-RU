---
title: Функция SAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Возвращает значение компонента насыщенности цвета.
ms.openlocfilehash: 3b3fd8e13ca9af4f0aea00d2f78c7b5c27be1932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415007"
---
# <a name="sat-function"></a><span data-ttu-id="ed8e0-103">Функция SAT</span><span class="sxs-lookup"><span data-stu-id="ed8e0-103">SAT Function</span></span>

<span data-ttu-id="ed8e0-104">Возвращает значение компонента насыщенности цвета.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed8e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed8e0-105">Syntax</span></span>

<span data-ttu-id="ed8e0-106">Кот (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ed8e0-106">SAT(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed8e0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed8e0-107">Parameters</span></span>

|<span data-ttu-id="ed8e0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ed8e0-108">**Name**</span></span>|<span data-ttu-id="ed8e0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ed8e0-109">**Required/Optional**</span></span>|<span data-ttu-id="ed8e0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ed8e0-110">**Data Type**</span></span>|<span data-ttu-id="ed8e0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed8e0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed8e0-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ed8e0-112">_expression_</span></span> <br/> |<span data-ttu-id="ed8e0-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ed8e0-113">Required</span></span>  <br/> |<span data-ttu-id="ed8e0-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="ed8e0-114">**Varies**</span></span> <br/> |<span data-ttu-id="ed8e0-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ed8e0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed8e0-116">Return value</span></span>

<span data-ttu-id="ed8e0-117">Числовой</span><span class="sxs-lookup"><span data-stu-id="ed8e0-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed8e0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed8e0-118">Remarks</span></span>

<span data-ttu-id="ed8e0-119">Возвращаемое значение — число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="ed8e0-120">Функция возвращает значение 0 для недопустимых входных данных.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-120">The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ed8e0-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed8e0-121">Example 1</span></span>

<span data-ttu-id="ed8e0-122">Кот (sheet. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="ed8e0-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ed8e0-123">Возвращает насыщенность цвета переднего плана листа. 4's.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ed8e0-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ed8e0-124">Example 2</span></span>

<span data-ttu-id="ed8e0-125">КОТ (8)</span><span class="sxs-lookup"><span data-stu-id="ed8e0-125">SAT(8)</span></span>
  
<span data-ttu-id="ed8e0-126">Возвращает 240, если документ использует цветовую палитру Visio по умолчанию, где темно-красный — цвет с индексом 8.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ed8e0-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ed8e0-127">Example 3</span></span>

<span data-ttu-id="ed8e0-128">СБ (HSL (, 10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ed8e0-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="ed8e0-129">Возвращает значение 20.</span><span class="sxs-lookup"><span data-stu-id="ed8e0-129">Returns 20.</span></span>
  

