---
title: Функция LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Возвращает значение компонента яркости цвета.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357983"
---
# <a name="lum-function"></a><span data-ttu-id="63689-103">Функция LUM</span><span class="sxs-lookup"><span data-stu-id="63689-103">LUM Function</span></span>

<span data-ttu-id="63689-104">Возвращает значение компонента яркости цвета.</span><span class="sxs-lookup"><span data-stu-id="63689-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="63689-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63689-105">Syntax</span></span>

<span data-ttu-id="63689-106">ЯРКОСТЬ (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="63689-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="63689-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63689-107">Parameters</span></span>

|<span data-ttu-id="63689-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="63689-108">**Name**</span></span>|<span data-ttu-id="63689-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="63689-109">**Required/Optional**</span></span>|<span data-ttu-id="63689-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="63689-110">**Data Type**</span></span>|<span data-ttu-id="63689-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63689-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="63689-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="63689-112">_expression_</span></span> <br/> |<span data-ttu-id="63689-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63689-113">Required</span></span>  <br/> |<span data-ttu-id="63689-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="63689-114">**Numeric**</span></span> <br/> |<span data-ttu-id="63689-115">Индекс цвета в таблице цветов документа или ссылка на ячейку, содержащую цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="63689-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="63689-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63689-116">Return value</span></span>

<span data-ttu-id="63689-117">Номер</span><span class="sxs-lookup"><span data-stu-id="63689-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63689-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="63689-118">Remarks</span></span>

<span data-ttu-id="63689-119">Возвращаемое значение — число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="63689-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="63689-120">Функция возвращает значение 0 для недопустимых входных данных.</span><span class="sxs-lookup"><span data-stu-id="63689-120">The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="63689-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63689-121">Example 1</span></span>

<span data-ttu-id="63689-122">ЯРКОСТЬ (sheet. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="63689-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="63689-123">Возвращает яркость листа. 4's заливки текста.</span><span class="sxs-lookup"><span data-stu-id="63689-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="63689-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63689-124">Example 2</span></span>

<span data-ttu-id="63689-125">ЯРКОСТЬ (6)</span><span class="sxs-lookup"><span data-stu-id="63689-125">LUM(6)</span></span>
  
<span data-ttu-id="63689-126">Возвращает 120, если документ использует цветовую палитру Visio по умолчанию, где пурпурный — цвет с индексом 6.</span><span class="sxs-lookup"><span data-stu-id="63689-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="63689-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="63689-127">Example 3</span></span>

<span data-ttu-id="63689-128">ЯРКОСТЬ (HSL (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="63689-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="63689-129">Возвращает значение 30.</span><span class="sxs-lookup"><span data-stu-id="63689-129">Returns 30.</span></span>
  

