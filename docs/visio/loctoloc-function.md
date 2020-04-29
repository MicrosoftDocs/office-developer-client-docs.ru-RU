---
title: Функция LOCTOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Возвращает преобразованную точку в локальных координатах в конечной системе координат.
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427488"
---
# <a name="loctoloc-function"></a><span data-ttu-id="99b2f-103">Функция LOCTOLOC</span><span class="sxs-lookup"><span data-stu-id="99b2f-103">LOCTOLOC Function</span></span>

<span data-ttu-id="99b2f-104">Возвращает преобразованную точку в локальных координатах в конечной системе координат.</span><span class="sxs-lookup"><span data-stu-id="99b2f-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="99b2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99b2f-105">Syntax</span></span>

<span data-ttu-id="99b2f-106">LOCTOLOC (\* \* *сркпоинт* \* \*, \* \* *сркреф* \* \*, \* \* *дстреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="99b2f-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="99b2f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="99b2f-107">Parameters</span></span>

|<span data-ttu-id="99b2f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="99b2f-108">**Name**</span></span>|<span data-ttu-id="99b2f-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="99b2f-109">**Required/Optional**</span></span>|<span data-ttu-id="99b2f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="99b2f-110">**Data Type**</span></span>|<span data-ttu-id="99b2f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="99b2f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="99b2f-112">_сркпоинт_</span><span class="sxs-lookup"><span data-stu-id="99b2f-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="99b2f-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="99b2f-113">Required</span></span>  <br/> |<span data-ttu-id="99b2f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="99b2f-114">**String**</span></span> <br/> | <span data-ttu-id="99b2f-115">Точка в локальных координатах в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="99b2f-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="99b2f-116">_сркреф_</span><span class="sxs-lookup"><span data-stu-id="99b2f-116">_srcRef_</span></span> <br/> |<span data-ttu-id="99b2f-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="99b2f-117">Required</span></span>  <br/> |<span data-ttu-id="99b2f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="99b2f-118">**String**</span></span> <br/> | <span data-ttu-id="99b2f-119">Ссылка на ячейку в исходном объекте.</span><span class="sxs-lookup"><span data-stu-id="99b2f-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="99b2f-120">_дстреф_</span><span class="sxs-lookup"><span data-stu-id="99b2f-120">_dstRef_</span></span> <br/> |<span data-ttu-id="99b2f-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="99b2f-121">Required</span></span>  <br/> |<span data-ttu-id="99b2f-122">**String**</span><span class="sxs-lookup"><span data-stu-id="99b2f-122">**String**</span></span> <br/> | <span data-ttu-id="99b2f-123">Ссылка на ячейку в целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="99b2f-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="99b2f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99b2f-124">Return value</span></span>

<span data-ttu-id="99b2f-125">String</span><span class="sxs-lookup"><span data-stu-id="99b2f-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99b2f-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="99b2f-126">Remarks</span></span>

<span data-ttu-id="99b2f-127">Функция LOCTOLOC преобразует точку из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="99b2f-127">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape.</span></span> <span data-ttu-id="99b2f-128">Эту функцию можно использовать для создания фигуры, например, с точки зрения точки из другого координатного пространства.</span><span class="sxs-lookup"><span data-stu-id="99b2f-128">You can use this function to construct a shape, for example, in terms of a point from another coordinate space.</span></span> <span data-ttu-id="99b2f-129">Эту функцию также можно использовать для преобразования локальной точки в координаты страницы или наоборот.</span><span class="sxs-lookup"><span data-stu-id="99b2f-129">You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="99b2f-130">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="99b2f-130">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="99b2f-131">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="99b2f-131">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="99b2f-132">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="99b2f-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="99b2f-133">Пример</span><span class="sxs-lookup"><span data-stu-id="99b2f-133">Example</span></span>

<span data-ttu-id="99b2f-134">Следующая формула преобразует локальный ПИН-код фигуры, связанной с формулой, в точку на странице.</span><span class="sxs-lookup"><span data-stu-id="99b2f-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


