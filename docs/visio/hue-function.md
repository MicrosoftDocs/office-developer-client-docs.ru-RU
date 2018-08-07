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
description: Возвращает значение компонента тона цвета.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813919"
---
# <a name="hue-function"></a><span data-ttu-id="a4bd0-103">Функция HUE</span><span class="sxs-lookup"><span data-stu-id="a4bd0-103">HUE Function</span></span>

<span data-ttu-id="a4bd0-104">Возвращает значение компонента тона цвета.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a4bd0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4bd0-105">Syntax</span></span>

<span data-ttu-id="a4bd0-106">ТОНА (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="a4bd0-106">HUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a4bd0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4bd0-107">Parameters</span></span>

|<span data-ttu-id="a4bd0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a4bd0-108">**Name**</span></span>|<span data-ttu-id="a4bd0-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="a4bd0-109">**Required/Optional**</span></span>|<span data-ttu-id="a4bd0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a4bd0-110">**Data Type**</span></span>|<span data-ttu-id="a4bd0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a4bd0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a4bd0-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="a4bd0-112">_expression_</span></span> <br/> |<span data-ttu-id="a4bd0-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a4bd0-113">Required</span></span>  <br/> |<span data-ttu-id="a4bd0-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a4bd0-114">**String**</span></span> <br/> |<span data-ttu-id="a4bd0-115">Выражение, которое оценивается как цвет.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a4bd0-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a4bd0-116">Return value</span></span>

<span data-ttu-id="a4bd0-117">Number</span><span class="sxs-lookup"><span data-stu-id="a4bd0-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4bd0-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4bd0-118">Remarks</span></span>

<span data-ttu-id="a4bd0-119">Возвращаемое значение — число в диапазоне 0 для 239 включительно.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-119">The return value is a number in the range 0 to 239, inclusive.</span></span> <span data-ttu-id="a4bd0-120">Входные данные является индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL) или ссылка на ячейку, которая содержит индекс цвета или цвет результатов.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-120">The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span> <span data-ttu-id="a4bd0-121">Функция возвращает 0 для недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-121">The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a4bd0-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4bd0-122">Example 1</span></span>

<span data-ttu-id="a4bd0-123">ТОНА (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="a4bd0-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="a4bd0-124">Возвращает цветовым цвет заливки Sheet. 4.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a4bd0-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a4bd0-125">Example 2</span></span>

<span data-ttu-id="a4bd0-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="a4bd0-126">HUE(7)</span></span>
  
<span data-ttu-id="a4bd0-127">Возвращает 120, если в документе используется по умолчанию Microsoft Visio цветовой палитры, в котором голубой цвет по индексу 7.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a4bd0-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a4bd0-128">Example 3</span></span>

<span data-ttu-id="a4bd0-129">ТОНА (HSL (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="a4bd0-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="a4bd0-130">Возвращает значение 10.</span><span class="sxs-lookup"><span data-stu-id="a4bd0-130">Returns 10.</span></span>
  

