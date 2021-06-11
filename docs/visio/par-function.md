---
title: Функция PAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Возвращает координаты точки в системе координат родительской фигуры.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414510"
---
# <a name="par-function"></a><span data-ttu-id="78239-103">Функция PAR</span><span class="sxs-lookup"><span data-stu-id="78239-103">PAR Function</span></span>

<span data-ttu-id="78239-104">Возвращает  _координаты точки в_ системе координат родительской фигуры.</span><span class="sxs-lookup"><span data-stu-id="78239-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78239-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78239-105">Syntax</span></span>

<span data-ttu-id="78239-106">PAR(\*\* *point* \*\* )</span><span class="sxs-lookup"><span data-stu-id="78239-106">PAR(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78239-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78239-107">Parameters</span></span>

|<span data-ttu-id="78239-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="78239-108">**Name**</span></span>|<span data-ttu-id="78239-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="78239-109">**Required/Optional**</span></span>|<span data-ttu-id="78239-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="78239-110">**Data Type**</span></span>|<span data-ttu-id="78239-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78239-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78239-112">_точка_</span><span class="sxs-lookup"><span data-stu-id="78239-112">_point_</span></span> <br/> |<span data-ttu-id="78239-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="78239-113">Required</span></span>  <br/> |<span data-ttu-id="78239-114">**Номер, номер**</span><span class="sxs-lookup"><span data-stu-id="78239-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="78239-115">Координаты точки в системе координат текущей формы.</span><span class="sxs-lookup"><span data-stu-id="78239-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78239-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="78239-116">Remarks</span></span>

<span data-ttu-id="78239-117">В microsoft Visio точка — это одно значение, которое олицетворяет пару *х* и *y-координат.*</span><span class="sxs-lookup"><span data-stu-id="78239-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="78239-118">Если фигура находится в группе, ее родителем является группа.</span><span class="sxs-lookup"><span data-stu-id="78239-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="78239-119">Если фигура не находится в группе, ее родителем является страница.</span><span class="sxs-lookup"><span data-stu-id="78239-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="78239-120">Пример</span><span class="sxs-lookup"><span data-stu-id="78239-120">Example</span></span>

<span data-ttu-id="78239-121">PAR(PNT(PinX,Piny))</span><span class="sxs-lookup"><span data-stu-id="78239-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="78239-122">В этом выражении PNT преобразует пару координат в текущей форме в точку.</span><span class="sxs-lookup"><span data-stu-id="78239-122">In this expression, PNT converts a pair of coordinates in the current shape into a point.</span></span> <span data-ttu-id="78239-123">Затем PAR преобразует точку в пару координат по отношению к нижнему левом углу страницы или группы, которая содержит текущую форму.</span><span class="sxs-lookup"><span data-stu-id="78239-123">PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

