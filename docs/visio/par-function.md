---
title: Параметр ИМЕЕТ функции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Возвращает x, y координаты точки в системе координат родительского фигуры.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814352"
---
# <a name="par-function"></a><span data-ttu-id="bde67-103">Параметр ИМЕЕТ функции</span><span class="sxs-lookup"><span data-stu-id="bde67-103">PAR Function</span></span>

<span data-ttu-id="bde67-104">Возвращает координаты _x, y_ точки в системе координат родительского фигуры.</span><span class="sxs-lookup"><span data-stu-id="bde67-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bde67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bde67-105">Syntax</span></span>

<span data-ttu-id="bde67-106">Параметр ИМЕЕТ (** *пункт* **)</span><span class="sxs-lookup"><span data-stu-id="bde67-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bde67-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bde67-107">Parameters</span></span>

|<span data-ttu-id="bde67-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bde67-108">**Name**</span></span>|<span data-ttu-id="bde67-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bde67-109">**Required/Optional**</span></span>|<span data-ttu-id="bde67-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bde67-110">**Data Type**</span></span>|<span data-ttu-id="bde67-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bde67-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bde67-112">_точка_</span><span class="sxs-lookup"><span data-stu-id="bde67-112">_point_</span></span> <br/> |<span data-ttu-id="bde67-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bde67-113">Required</span></span>  <br/> |<span data-ttu-id="bde67-114">**Номер, номер**</span><span class="sxs-lookup"><span data-stu-id="bde67-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="bde67-115">Координаты точки в системе координат текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="bde67-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bde67-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="bde67-116">Remarks</span></span>

<span data-ttu-id="bde67-117">В Microsoft Visio точки — это одно значение, которое реализует пары *x* - и *y* -координаты.</span><span class="sxs-lookup"><span data-stu-id="bde67-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="bde67-118">Если фигуры в группе, родительского — группа.</span><span class="sxs-lookup"><span data-stu-id="bde67-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="bde67-119">Если фигура не является группу, его родителя является страницы.</span><span class="sxs-lookup"><span data-stu-id="bde67-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bde67-120">Пример</span><span class="sxs-lookup"><span data-stu-id="bde67-120">Example</span></span>

<span data-ttu-id="bde67-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="bde67-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="bde67-122">В это выражение раздела PNT преобразует пары координат текущего фигуры в точку.</span><span class="sxs-lookup"><span data-stu-id="bde67-122">In this expression, PNT converts a pair of coordinates in the current shape into a point.</span></span> <span data-ttu-id="bde67-123">Параметр ИМЕЕТ затем преобразует точку в пары координат при использовании нижнем левом углу страницы или группа, содержащая текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="bde67-123">PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

