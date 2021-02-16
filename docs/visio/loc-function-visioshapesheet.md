---
title: LOC Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Принимает точку, определяемую в локальных координатах одной фигуры, и возвращает эквивалентную точку, выраженную в локальных координатах фигуры, связанной с формулой.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422427"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="5910e-103">LOC Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5910e-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5910e-104">Принимает точку, определяемую в локальных координатах одной фигуры, и возвращает эквивалентную точку, выраженную в локальных координатах фигуры, связанной с формулой.</span><span class="sxs-lookup"><span data-stu-id="5910e-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5910e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5910e-105">Syntax</span></span>

<span data-ttu-id="5910e-106">LOC(\*\* *point* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5910e-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5910e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5910e-107">Parameters</span></span>

|<span data-ttu-id="5910e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5910e-108">**Name**</span></span>|<span data-ttu-id="5910e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5910e-109">**Required/Optional**</span></span>|<span data-ttu-id="5910e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5910e-110">**Data Type**</span></span>|<span data-ttu-id="5910e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5910e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5910e-112">_point_</span><span class="sxs-lookup"><span data-stu-id="5910e-112">_point_</span></span> <br/> |<span data-ttu-id="5910e-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5910e-113">Required</span></span>  <br/> |<span data-ttu-id="5910e-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="5910e-114">**String**</span></span> <br/> | <span data-ttu-id="5910e-115">Точка, определяемая в локальных координатах одной фигуры.</span><span class="sxs-lookup"><span data-stu-id="5910e-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5910e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5910e-116">Return value</span></span>

<span data-ttu-id="5910e-117">String</span><span class="sxs-lookup"><span data-stu-id="5910e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5910e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5910e-118">Remarks</span></span>

<span data-ttu-id="5910e-119">Локальные координаты измеряются из левого нижнего угла прямоугольника выделения фигуры.</span><span class="sxs-lookup"><span data-stu-id="5910e-119">Local coordinates are measured from the lower-left corner of the shape's selection rectangle.</span></span> <span data-ttu-id="5910e-120">Обе фигуры должны быть на одной странице.</span><span class="sxs-lookup"><span data-stu-id="5910e-120">Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="5910e-121">Пример</span><span class="sxs-lookup"><span data-stu-id="5910e-121">Example</span></span>

<span data-ttu-id="5910e-122">LOC(PNT(Sheet.5! LocPinX, Sheet.5! LocPinY))</span><span class="sxs-lookup"><span data-stu-id="5910e-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="5910e-123">В этом выражении PNT преобразует набор локальных координат в листе Sheet.5 в точку.</span><span class="sxs-lookup"><span data-stu-id="5910e-123">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point.</span></span> <span data-ttu-id="5910e-124">(Лист.5 — это другая фигура на той же странице рисования.) Затем LOC преобразует эту точку в эквивалентную точку в локальной системе координат текущей фигуры относительно левого нижнего угла прямоугольника выделения текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="5910e-124">(Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="5910e-125">5 в листе Sheet.5 — это номер ИД фигуры, который отображается в диалоговом окне **"Имя** фигуры" (вкладка **"Разработчик").**</span><span class="sxs-lookup"><span data-stu-id="5910e-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

