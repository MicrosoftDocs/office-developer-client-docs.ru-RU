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
# <a name="sat-function"></a><span data-ttu-id="bba07-103">Функция SAT</span><span class="sxs-lookup"><span data-stu-id="bba07-103">SAT Function</span></span>

<span data-ttu-id="bba07-104">Возвращает значение компонента насыщенности цвета.</span><span class="sxs-lookup"><span data-stu-id="bba07-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bba07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bba07-105">Syntax</span></span>

<span data-ttu-id="bba07-106">SAT(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="bba07-106">SAT(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bba07-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba07-107">Parameters</span></span>

|<span data-ttu-id="bba07-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bba07-108">**Name**</span></span>|<span data-ttu-id="bba07-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="bba07-109">**Required/Optional**</span></span>|<span data-ttu-id="bba07-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bba07-110">**Data Type**</span></span>|<span data-ttu-id="bba07-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bba07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bba07-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="bba07-112">_expression_</span></span> <br/> |<span data-ttu-id="bba07-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bba07-113">Required</span></span>  <br/> |<span data-ttu-id="bba07-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="bba07-114">**Varies**</span></span> <br/> |<span data-ttu-id="bba07-115">Индекс цвета в таблице цветов документа, выражение, разрешаемого в пользовательский цвет (например, RGB или HSL) или ссылка на ячейку, содержаную индекс цвета или результат цвета.</span><span class="sxs-lookup"><span data-stu-id="bba07-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bba07-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bba07-116">Return value</span></span>

<span data-ttu-id="bba07-117">Числовой</span><span class="sxs-lookup"><span data-stu-id="bba07-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bba07-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="bba07-118">Remarks</span></span>

<span data-ttu-id="bba07-119">Возвращаемая величина — это число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="bba07-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="bba07-120">Функция возвращает 0 для недопустимого ввода.</span><span class="sxs-lookup"><span data-stu-id="bba07-120">The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="bba07-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bba07-121">Example 1</span></span>

<span data-ttu-id="bba07-122">SAT(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="bba07-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="bba07-123">Возвращает насыщенность цвета переднего плана заливки Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="bba07-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bba07-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bba07-124">Example 2</span></span>

<span data-ttu-id="bba07-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="bba07-125">SAT(8)</span></span>
  
<span data-ttu-id="bba07-126">Возвращает значение 240, если документ использует цветовую палитру Visio по умолчанию, где темно-красный цвет — это цвет в индексе 8.</span><span class="sxs-lookup"><span data-stu-id="bba07-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bba07-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bba07-127">Example 3</span></span>

<span data-ttu-id="bba07-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="bba07-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="bba07-129">Возвращает 20.</span><span class="sxs-lookup"><span data-stu-id="bba07-129">Returns 20.</span></span>
  

