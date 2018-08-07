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
description: Возвращает ломаной. Эта функция используется в ячейке A геометрических рядов PolyLineTo.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814389"
---
# <a name="polyline-function"></a><span data-ttu-id="a68c3-104">Функция POLYLINE</span><span class="sxs-lookup"><span data-stu-id="a68c3-104">POLYLINE Function</span></span>

<span data-ttu-id="a68c3-105">Возвращает ломаной.</span><span class="sxs-lookup"><span data-stu-id="a68c3-105">Returns a polyline.</span></span> <span data-ttu-id="a68c3-106">Эта функция используется в ячейке A геометрических рядов PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="a68c3-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a68c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a68c3-107">Syntax</span></span>

<span data-ttu-id="a68c3-108">POLYLINE (** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span><span class="sxs-lookup"><span data-stu-id="a68c3-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a68c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a68c3-109">Parameters</span></span>

|<span data-ttu-id="a68c3-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a68c3-110">**Name**</span></span>|<span data-ttu-id="a68c3-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="a68c3-111">**Required/Optional**</span></span>|<span data-ttu-id="a68c3-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a68c3-112">**Data Type**</span></span>|<span data-ttu-id="a68c3-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a68c3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a68c3-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="a68c3-114">_xType_</span></span> <br/> |<span data-ttu-id="a68c3-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a68c3-115">Required</span></span>  <br/> |<span data-ttu-id="a68c3-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a68c3-116">**Boolean**</span></span> <br/> |<span data-ttu-id="a68c3-117">Указывает способ представления входных данных _x_ .</span><span class="sxs-lookup"><span data-stu-id="a68c3-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="a68c3-118">Если _xType_ имеет значение 0, входные данные _x_-интерпретации данных в процентах от ширины.</span><span class="sxs-lookup"><span data-stu-id="a68c3-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="a68c3-119">Если _xType_ -1, входные данные _x_-данных интерпретируется как локальный координата.</span><span class="sxs-lookup"><span data-stu-id="a68c3-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a68c3-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="a68c3-120">_yType_</span></span> <br/> |<span data-ttu-id="a68c3-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a68c3-121">Required</span></span>  <br/> |<span data-ttu-id="a68c3-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a68c3-122">**Boolean**</span></span> <br/> |<span data-ttu-id="a68c3-123">Указывает способ интерпретации _y_-вводить данные.</span><span class="sxs-lookup"><span data-stu-id="a68c3-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="a68c3-124">Если _yType_ имеет значение 0, входные данные _y_-интерпретации данных в процентном соотношении от высоту.</span><span class="sxs-lookup"><span data-stu-id="a68c3-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="a68c3-125">Если _yType_ -1, входные данные _y_-данных интерпретируется как локальный координата.</span><span class="sxs-lookup"><span data-stu-id="a68c3-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a68c3-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="a68c3-126">_x1_</span></span> <br/> |<span data-ttu-id="a68c3-127">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a68c3-127">Required</span></span>  <br/> |<span data-ttu-id="a68c3-128">**Число**</span><span class="sxs-lookup"><span data-stu-id="a68c3-128">**Number**</span></span> <br/> | <span data-ttu-id="a68c3-129">_X_-координации усилий.</span><span class="sxs-lookup"><span data-stu-id="a68c3-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="a68c3-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="a68c3-130">_y1_</span></span> <br/> |<span data-ttu-id="a68c3-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a68c3-131">Required</span></span>  <br/> |<span data-ttu-id="a68c3-132">**Число**</span><span class="sxs-lookup"><span data-stu-id="a68c3-132">**Number**</span></span> <br/> |<span data-ttu-id="a68c3-133">_Y_— координации усилий.</span><span class="sxs-lookup"><span data-stu-id="a68c3-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a68c3-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="a68c3-134">Remarks</span></span>

<span data-ttu-id="a68c3-135">Для каждого аргумента *x* значения *y* аргумент; в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a68c3-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a68c3-136">Пример</span><span class="sxs-lookup"><span data-stu-id="a68c3-136">Example</span></span>

<span data-ttu-id="a68c3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="a68c3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="a68c3-138">Возвращает прямоугольник измерения ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="a68c3-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

