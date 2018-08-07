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
description: Возвращает значение синего компонента цвета. Возвращаемое значение представляет собой целое число в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недопустимые данные.
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813284"
---
# <a name="blue-function"></a><span data-ttu-id="4a7d2-105">Функция BLUE</span><span class="sxs-lookup"><span data-stu-id="4a7d2-105">BLUE Function</span></span>

<span data-ttu-id="4a7d2-106">Возвращает значение синего компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-106">Returns the blue component of a color.</span></span> <span data-ttu-id="4a7d2-107">Возвращаемое значение представляет собой целое число в диапазоне от 0 до 255 включительно.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="4a7d2-108">Функция возвращает 0 для недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a7d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a7d2-109">Syntax</span></span>

<span data-ttu-id="4a7d2-110">СИНИЙ (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="4a7d2-110">BLUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a7d2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a7d2-111">Parameters</span></span>

|<span data-ttu-id="4a7d2-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-112">**Name**</span></span>|<span data-ttu-id="4a7d2-113">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-113">**Required/Optional**</span></span>|<span data-ttu-id="4a7d2-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-114">**Data Type**</span></span>|<span data-ttu-id="4a7d2-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a7d2-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="4a7d2-116">_expression_</span></span> <br/> |<span data-ttu-id="4a7d2-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4a7d2-117">Required</span></span>  <br/> |<span data-ttu-id="4a7d2-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4a7d2-118">**String**</span></span> <br/> |<span data-ttu-id="4a7d2-119">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL) или ссылку на ячейку, содержащую цвет индекса или цветовой результатов.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4a7d2-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4a7d2-120">Return value</span></span>

<span data-ttu-id="4a7d2-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="4a7d2-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="4a7d2-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a7d2-122">Example 1</span></span>

<span data-ttu-id="4a7d2-123">СИНИЙ (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="4a7d2-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="4a7d2-124">Возвращает значение синего компонента цвет заливки Sheet. 4.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4a7d2-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4a7d2-125">Example 2</span></span>

<span data-ttu-id="4a7d2-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="4a7d2-126">BLUE(13)</span></span>
  
<span data-ttu-id="4a7d2-127">Возвращает 128, если в документе используется по умолчанию Visio цветовой палитры, в котором голубой цвет по индексу 13.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4a7d2-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4a7d2-128">Example 3</span></span>

<span data-ttu-id="4a7d2-129">СИНИЙ (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="4a7d2-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="4a7d2-130">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="4a7d2-130">Returns 30.</span></span>
  

