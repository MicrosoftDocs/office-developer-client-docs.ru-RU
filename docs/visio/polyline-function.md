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
description: Возвращает многолинейную линию. Эта функция используется в ячейке A геометрических строк PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426298"
---
# <a name="polyline-function"></a><span data-ttu-id="d0bde-104">Функция POLYLINE</span><span class="sxs-lookup"><span data-stu-id="d0bde-104">POLYLINE Function</span></span>

<span data-ttu-id="d0bde-105">Возвращает многолинейную линию.</span><span class="sxs-lookup"><span data-stu-id="d0bde-105">Returns a polyline.</span></span> <span data-ttu-id="d0bde-106">Эта функция используется в ячейке A геометрических строк PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="d0bde-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d0bde-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0bde-107">Syntax</span></span>

<span data-ttu-id="d0bde-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span><span class="sxs-lookup"><span data-stu-id="d0bde-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0bde-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0bde-109">Parameters</span></span>

|<span data-ttu-id="d0bde-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d0bde-110">**Name**</span></span>|<span data-ttu-id="d0bde-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d0bde-111">**Required/Optional**</span></span>|<span data-ttu-id="d0bde-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d0bde-112">**Data Type**</span></span>|<span data-ttu-id="d0bde-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d0bde-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0bde-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="d0bde-114">_xType_</span></span> <br/> |<span data-ttu-id="d0bde-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d0bde-115">Required</span></span>  <br/> |<span data-ttu-id="d0bde-116">**Логический**</span><span class="sxs-lookup"><span data-stu-id="d0bde-116">**Boolean**</span></span> <br/> |<span data-ttu-id="d0bde-117">Указывает, как интерпретировать _входные данные x._</span><span class="sxs-lookup"><span data-stu-id="d0bde-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="d0bde-118">Если  _xType_ имеет 0, входные  _данные x-data_ интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="d0bde-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="d0bde-119">Если  _xType_ имеет 1,  _входные данные x-data_ интерпретируются как локализованная координата.</span><span class="sxs-lookup"><span data-stu-id="d0bde-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="d0bde-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="d0bde-120">_yType_</span></span> <br/> |<span data-ttu-id="d0bde-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d0bde-121">Required</span></span>  <br/> |<span data-ttu-id="d0bde-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="d0bde-122">**Boolean**</span></span> <br/> |<span data-ttu-id="d0bde-123">Указывает, как интерпретировать _входные данные y._</span><span class="sxs-lookup"><span data-stu-id="d0bde-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="d0bde-124">Если  _yType_ имеет 0,  _входные данные y_-data интерпретируются как процент высоты.</span><span class="sxs-lookup"><span data-stu-id="d0bde-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="d0bde-125">Если  _yType_ имеет 1,  _входные данные y_-data интерпретируются как локализованная координата.</span><span class="sxs-lookup"><span data-stu-id="d0bde-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="d0bde-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="d0bde-126">_x1_</span></span> <br/> |<span data-ttu-id="d0bde-127">Обязательна</span><span class="sxs-lookup"><span data-stu-id="d0bde-127">Required</span></span>  <br/> |<span data-ttu-id="d0bde-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0bde-128">**Number**</span></span> <br/> | <span data-ttu-id="d0bde-129">X-координата. </span><span class="sxs-lookup"><span data-stu-id="d0bde-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="d0bde-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="d0bde-130">_y1_</span></span> <br/> |<span data-ttu-id="d0bde-131">Обязательна</span><span class="sxs-lookup"><span data-stu-id="d0bde-131">Required</span></span>  <br/> |<span data-ttu-id="d0bde-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0bde-132">**Number**</span></span> <br/> |<span data-ttu-id="d0bde-133">Координата _Y._</span><span class="sxs-lookup"><span data-stu-id="d0bde-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0bde-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0bde-134">Remarks</span></span>

<span data-ttu-id="d0bde-135">Для каждого  *аргумента x*  должен быть аргумент  *y;*  в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0bde-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d0bde-136">Пример</span><span class="sxs-lookup"><span data-stu-id="d0bde-136">Example</span></span>

<span data-ttu-id="d0bde-137">POLYLINE (0, 0, 0, 0, 1, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="d0bde-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="d0bde-138">Возвращает прямоугольник размеров Width x Height.</span><span class="sxs-lookup"><span data-stu-id="d0bde-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

