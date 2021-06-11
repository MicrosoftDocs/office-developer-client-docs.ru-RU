---
title: Функция POLYLINE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Возвращает полилин. Эта функция используется в строках геометрии A в строках геометрии PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426298"
---
# <a name="polyline-function"></a><span data-ttu-id="28c5a-104">Функция POLYLINE</span><span class="sxs-lookup"><span data-stu-id="28c5a-104">POLYLINE Function</span></span>

<span data-ttu-id="28c5a-105">Возвращает полилин.</span><span class="sxs-lookup"><span data-stu-id="28c5a-105">Returns a polyline.</span></span> <span data-ttu-id="28c5a-106">Эта функция используется в строках геометрии A в строках геометрии PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="28c5a-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28c5a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28c5a-107">Syntax</span></span>

<span data-ttu-id="28c5a-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span><span class="sxs-lookup"><span data-stu-id="28c5a-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28c5a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28c5a-109">Parameters</span></span>

|<span data-ttu-id="28c5a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="28c5a-110">**Name**</span></span>|<span data-ttu-id="28c5a-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="28c5a-111">**Required/Optional**</span></span>|<span data-ttu-id="28c5a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="28c5a-112">**Data Type**</span></span>|<span data-ttu-id="28c5a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="28c5a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28c5a-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="28c5a-114">_xType_</span></span> <br/> |<span data-ttu-id="28c5a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="28c5a-115">Required</span></span>  <br/> |<span data-ttu-id="28c5a-116">**Логический**</span><span class="sxs-lookup"><span data-stu-id="28c5a-116">**Boolean**</span></span> <br/> |<span data-ttu-id="28c5a-117">Указывает, как интерпретировать _данные ввода x._</span><span class="sxs-lookup"><span data-stu-id="28c5a-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="28c5a-118">Если  _xType_ — 0,  _входные x-data_ интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="28c5a-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="28c5a-119">Если  _xType_ — 1,  _входные x-data_ интерпретируются как локализованные координаты.</span><span class="sxs-lookup"><span data-stu-id="28c5a-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="28c5a-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="28c5a-120">_yType_</span></span> <br/> |<span data-ttu-id="28c5a-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="28c5a-121">Required</span></span>  <br/> |<span data-ttu-id="28c5a-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="28c5a-122">**Boolean**</span></span> <br/> |<span data-ttu-id="28c5a-123">Указывает, как интерпретировать _данные ввода y._</span><span class="sxs-lookup"><span data-stu-id="28c5a-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="28c5a-124">Если  _yType_ — 0,  _входные данные y-data_ интерпретируются как процент высоты.</span><span class="sxs-lookup"><span data-stu-id="28c5a-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="28c5a-125">Если  _yType_ — 1,  _входные данные_ интерпретируются как локализованные координаты.</span><span class="sxs-lookup"><span data-stu-id="28c5a-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="28c5a-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="28c5a-126">_x1_</span></span> <br/> |<span data-ttu-id="28c5a-127">Обязательный</span><span class="sxs-lookup"><span data-stu-id="28c5a-127">Required</span></span>  <br/> |<span data-ttu-id="28c5a-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="28c5a-128">**Number**</span></span> <br/> | <span data-ttu-id="28c5a-129">X-coordinate. </span><span class="sxs-lookup"><span data-stu-id="28c5a-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="28c5a-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="28c5a-130">_y1_</span></span> <br/> |<span data-ttu-id="28c5a-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="28c5a-131">Required</span></span>  <br/> |<span data-ttu-id="28c5a-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="28c5a-132">**Number**</span></span> <br/> |<span data-ttu-id="28c5a-133">_A y-coordinate._</span><span class="sxs-lookup"><span data-stu-id="28c5a-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28c5a-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="28c5a-134">Remarks</span></span>

<span data-ttu-id="28c5a-135">Для каждого  *аргумента x*  должен быть  *аргумент y;*  в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="28c5a-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="28c5a-136">Пример</span><span class="sxs-lookup"><span data-stu-id="28c5a-136">Example</span></span>

<span data-ttu-id="28c5a-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="28c5a-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="28c5a-138">Возвращает прямоугольник размеров Width x Height.</span><span class="sxs-lookup"><span data-stu-id="28c5a-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

