---
title: Функция LOCTOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Возвращает преобразованную точку в родительских координатах в конечной системе координат.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314849"
---
# <a name="loctopar-function"></a><span data-ttu-id="3fc4e-103">Функция LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="3fc4e-103">LOCTOPAR Function</span></span>

<span data-ttu-id="3fc4e-104">Возвращает преобразованную точку в родительских координатах в конечной системе координат.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3fc4e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fc4e-105">Syntax</span></span>

<span data-ttu-id="3fc4e-106">LOCTOPAR (\* \* *сркпоинт* \* \*, \* \* *сркреф* \* \*, \* \* *дстреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3fc4e-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3fc4e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fc4e-107">Parameters</span></span>

|<span data-ttu-id="3fc4e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-108">**Name**</span></span>|<span data-ttu-id="3fc4e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-109">**Required/Optional**</span></span>|<span data-ttu-id="3fc4e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-110">**Data Type**</span></span>|<span data-ttu-id="3fc4e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3fc4e-112">_Сркпоинт_</span><span class="sxs-lookup"><span data-stu-id="3fc4e-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="3fc4e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fc4e-113">Required</span></span>  <br/> |<span data-ttu-id="3fc4e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-114">**String**</span></span> <br/> | <span data-ttu-id="3fc4e-115">Точка в локальных координатах в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="3fc4e-116">_Сркреф_</span><span class="sxs-lookup"><span data-stu-id="3fc4e-116">_srcRef_</span></span> <br/> |<span data-ttu-id="3fc4e-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fc4e-117">Required</span></span>  <br/> |<span data-ttu-id="3fc4e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-118">**String**</span></span> <br/> | <span data-ttu-id="3fc4e-119">Ссылка на ячейку в исходном объекте.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="3fc4e-120">_Дстреф_</span><span class="sxs-lookup"><span data-stu-id="3fc4e-120">_dstRef_</span></span> <br/> |<span data-ttu-id="3fc4e-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fc4e-121">Required</span></span>  <br/> |<span data-ttu-id="3fc4e-122">**String**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-122">**String**</span></span> <br/> | <span data-ttu-id="3fc4e-123">Ссылка на ячейку в целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3fc4e-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fc4e-124">Return value</span></span>

<span data-ttu-id="3fc4e-125">Строка</span><span class="sxs-lookup"><span data-stu-id="3fc4e-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fc4e-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="3fc4e-126">Remarks</span></span>

<span data-ttu-id="3fc4e-127">Преобразует точку из локальных координат исходной фигуры в родительские координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-127">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape.</span></span> <span data-ttu-id="3fc4e-128">Можно использовать функцию LOCTOPAR для установки родительских координат в ячейках, таких как PinX, PinY, BeginX и начало фигуры, с помощью другой точки из другой системы координат.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-128">You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="3fc4e-129">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-129">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="3fc4e-130">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-130">It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="3fc4e-131">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="3fc4e-132">Если объект Destination является страницей, не имеющей родителя, результат выражается в локальных координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3fc4e-133">Пример</span><span class="sxs-lookup"><span data-stu-id="3fc4e-133">Example</span></span>

<span data-ttu-id="3fc4e-134">LOCTOPAR (PNT (LocPinX, LocPinY), Width, Sheet. 4! Полноширинные</span><span class="sxs-lookup"><span data-stu-id="3fc4e-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="3fc4e-135">Преобразует локальный ПИН-код фигуры, связанной с формулой, в родительские координаты листа. 4.</span><span class="sxs-lookup"><span data-stu-id="3fc4e-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

