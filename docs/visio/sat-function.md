---
title: Функция Субботам
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Возвращает значение компонента насыщенность цвета.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814722"
---
# <a name="sat-function"></a><span data-ttu-id="a9de5-103">Функция Субботам</span><span class="sxs-lookup"><span data-stu-id="a9de5-103">SAT Function</span></span>

<span data-ttu-id="a9de5-104">Возвращает значение компонента насыщенность цвета.</span><span class="sxs-lookup"><span data-stu-id="a9de5-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9de5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9de5-105">Syntax</span></span>

<span data-ttu-id="a9de5-106">СБ (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="a9de5-106">SAT(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9de5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9de5-107">Parameters</span></span>

|<span data-ttu-id="a9de5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a9de5-108">**Name**</span></span>|<span data-ttu-id="a9de5-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="a9de5-109">**Required/Optional**</span></span>|<span data-ttu-id="a9de5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a9de5-110">**Data Type**</span></span>|<span data-ttu-id="a9de5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9de5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9de5-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="a9de5-112">_expression_</span></span> <br/> |<span data-ttu-id="a9de5-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a9de5-113">Required</span></span>  <br/> |<span data-ttu-id="a9de5-114">**Может отличаться**</span><span class="sxs-lookup"><span data-stu-id="a9de5-114">**Varies**</span></span> <br/> |<span data-ttu-id="a9de5-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL) или ссылку на ячейку, содержащую цвет индекса или цветовой результатов.</span><span class="sxs-lookup"><span data-stu-id="a9de5-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a9de5-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a9de5-116">Return value</span></span>

<span data-ttu-id="a9de5-117">Числовой</span><span class="sxs-lookup"><span data-stu-id="a9de5-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9de5-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9de5-118">Remarks</span></span>

<span data-ttu-id="a9de5-119">Возвращаемое значение — число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="a9de5-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="a9de5-120">Функция возвращает 0 для недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="a9de5-120">The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="a9de5-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9de5-121">Example 1</span></span>

<span data-ttu-id="a9de5-122">Суббота (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="a9de5-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="a9de5-123">Возвращает насыщенность цвет заливки Sheet. 4.</span><span class="sxs-lookup"><span data-stu-id="a9de5-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a9de5-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a9de5-124">Example 2</span></span>

<span data-ttu-id="a9de5-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="a9de5-125">SAT(8)</span></span>
  
<span data-ttu-id="a9de5-126">Возвращает 240, если в документе используется по умолчанию Visio цветовой палитры, в котором Темно-красный цвет по индексу 8.</span><span class="sxs-lookup"><span data-stu-id="a9de5-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a9de5-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a9de5-127">Example 3</span></span>

<span data-ttu-id="a9de5-128">СУББОТА (HSL (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="a9de5-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="a9de5-129">Возвращает 20.</span><span class="sxs-lookup"><span data-stu-id="a9de5-129">Returns 20.</span></span>
  

