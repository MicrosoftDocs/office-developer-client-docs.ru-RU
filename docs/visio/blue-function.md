---
title: Функция BLUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Возвращает синий компонент цвета. Возвращаемое значение — это целое число в диапазоне от 0 до 255 включительно. Функция возвращает значение 0 для недопустимых входных данных.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297356"
---
# <a name="blue-function"></a><span data-ttu-id="ea2c1-105">Функция BLUE</span><span class="sxs-lookup"><span data-stu-id="ea2c1-105">BLUE Function</span></span>

<span data-ttu-id="ea2c1-106">Возвращает синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-106">Returns the blue component of a color.</span></span> <span data-ttu-id="ea2c1-107">Возвращаемое значение — это целое число в диапазоне от 0 до 255 включительно.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="ea2c1-108">Функция возвращает значение 0 для недопустимых входных данных.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ea2c1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea2c1-109">Syntax</span></span>

<span data-ttu-id="ea2c1-110">BLUE (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ea2c1-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea2c1-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea2c1-111">Parameters</span></span>

|<span data-ttu-id="ea2c1-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ea2c1-112">**Name**</span></span>|<span data-ttu-id="ea2c1-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ea2c1-113">**Required/Optional**</span></span>|<span data-ttu-id="ea2c1-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ea2c1-114">**Data Type**</span></span>|<span data-ttu-id="ea2c1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea2c1-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea2c1-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ea2c1-116">_expression_</span></span> <br/> |<span data-ttu-id="ea2c1-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ea2c1-117">Required</span></span>  <br/> |<span data-ttu-id="ea2c1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ea2c1-118">**String**</span></span> <br/> |<span data-ttu-id="ea2c1-119">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ea2c1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea2c1-120">Return value</span></span>

<span data-ttu-id="ea2c1-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="ea2c1-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ea2c1-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea2c1-122">Example 1</span></span>

<span data-ttu-id="ea2c1-123">СИНИЙ (sheet. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="ea2c1-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ea2c1-124">Возвращает синий компонент листа лист. 4's заливки цветом текста.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ea2c1-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea2c1-125">Example 2</span></span>

<span data-ttu-id="ea2c1-126">СИНИЙ (13)</span><span class="sxs-lookup"><span data-stu-id="ea2c1-126">BLUE(13)</span></span>
  
<span data-ttu-id="ea2c1-127">Возвращает 128, если документ использует цветовую палитру Visio по умолчанию, где голубой — цвет с индексом 13.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ea2c1-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ea2c1-128">Example 3</span></span>

<span data-ttu-id="ea2c1-129">BLUE (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ea2c1-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="ea2c1-130">Возвращает значение 30.</span><span class="sxs-lookup"><span data-stu-id="ea2c1-130">Returns 30.</span></span>
  

