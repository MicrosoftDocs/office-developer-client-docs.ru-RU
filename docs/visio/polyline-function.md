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
description: Возвращает ломаную линию. Эта функция используется в ячейке в строках геометрических элементов для группы.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426298"
---
# <a name="polyline-function"></a><span data-ttu-id="5205d-104">Функция POLYLINE</span><span class="sxs-lookup"><span data-stu-id="5205d-104">POLYLINE Function</span></span>

<span data-ttu-id="5205d-105">Возвращает ломаную линию.</span><span class="sxs-lookup"><span data-stu-id="5205d-105">Returns a polyline.</span></span> <span data-ttu-id="5205d-106">Эта функция используется в ячейке в строках геометрических элементов для группы.</span><span class="sxs-lookup"><span data-stu-id="5205d-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5205d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5205d-107">Syntax</span></span>

<span data-ttu-id="5205d-108">ЛОМАная (\* \* *кстипе* \* \*, \* \* *итипе* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="5205d-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5205d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5205d-109">Parameters</span></span>

|<span data-ttu-id="5205d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5205d-110">**Name**</span></span>|<span data-ttu-id="5205d-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5205d-111">**Required/Optional**</span></span>|<span data-ttu-id="5205d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5205d-112">**Data Type**</span></span>|<span data-ttu-id="5205d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5205d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5205d-114">_Кстипе_</span><span class="sxs-lookup"><span data-stu-id="5205d-114">_xType_</span></span> <br/> |<span data-ttu-id="5205d-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5205d-115">Required</span></span>  <br/> |<span data-ttu-id="5205d-116">**Логический**</span><span class="sxs-lookup"><span data-stu-id="5205d-116">**Boolean**</span></span> <br/> |<span data-ttu-id="5205d-117">Указывает способ интерпретации входных данных _x_ .</span><span class="sxs-lookup"><span data-stu-id="5205d-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="5205d-118">Если _кстипе_ имеет значение 0, входные данные _x_-данных интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="5205d-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="5205d-119">Если _кстипе_ имеет значение 1, то входные данные _x_интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="5205d-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="5205d-120">_Итипе_</span><span class="sxs-lookup"><span data-stu-id="5205d-120">_yType_</span></span> <br/> |<span data-ttu-id="5205d-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5205d-121">Required</span></span>  <br/> |<span data-ttu-id="5205d-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="5205d-122">**Boolean**</span></span> <br/> |<span data-ttu-id="5205d-123">Указывает способ интерпретации входных данных _y_.</span><span class="sxs-lookup"><span data-stu-id="5205d-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="5205d-124">Если _итипе_ имеет значение 0, входные данные _y_интерпретируются как процент от высоты.</span><span class="sxs-lookup"><span data-stu-id="5205d-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="5205d-125">Если _итипе_ имеет значение 1, входные данные _y_интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="5205d-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="5205d-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="5205d-126">_x1_</span></span> <br/> |<span data-ttu-id="5205d-127">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5205d-127">Required</span></span>  <br/> |<span data-ttu-id="5205d-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="5205d-128">**Number**</span></span> <br/> | <span data-ttu-id="5205d-129">Координата _x_.</span><span class="sxs-lookup"><span data-stu-id="5205d-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="5205d-130">_Y1_</span><span class="sxs-lookup"><span data-stu-id="5205d-130">_y1_</span></span> <br/> |<span data-ttu-id="5205d-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5205d-131">Required</span></span>  <br/> |<span data-ttu-id="5205d-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="5205d-132">**Number**</span></span> <br/> |<span data-ttu-id="5205d-133">Координата _y_.</span><span class="sxs-lookup"><span data-stu-id="5205d-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5205d-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="5205d-134">Remarks</span></span>

<span data-ttu-id="5205d-135">Для каждого аргумента *x* должен быть аргумент *y* ; в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="5205d-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5205d-136">Пример</span><span class="sxs-lookup"><span data-stu-id="5205d-136">Example</span></span>

<span data-ttu-id="5205d-137">ЛОМАНАЯ ЛИНИЯ (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5205d-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="5205d-138">Возвращает прямоугольник с шириной x высота.</span><span class="sxs-lookup"><span data-stu-id="5205d-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

