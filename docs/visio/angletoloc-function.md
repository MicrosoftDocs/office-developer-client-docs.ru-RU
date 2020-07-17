---
title: Функция ANGLETOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Возвращает преобразованный угол в локальной системе координат конечной фигуры. Преобразует угол из локальных координат исходной фигуры в локальные координаты конечной фигуры.
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160267"
---
# <a name="angletoloc-function"></a><span data-ttu-id="96bb4-104">Функция ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="96bb4-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="96bb4-105">Возвращает преобразованный угол в локальной системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="96bb4-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="96bb4-106">Преобразует угол из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="96bb4-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="96bb4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96bb4-107">Syntax</span></span>

<span data-ttu-id="96bb4-108">ANGLETOLOC (***сркангле***, ***сркреф***, ***дстреф*** )</span><span class="sxs-lookup"><span data-stu-id="96bb4-108">ANGLETOLOC(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96bb4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="96bb4-109">Parameters</span></span>

|<span data-ttu-id="96bb4-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="96bb4-110">**Name**</span></span>|<span data-ttu-id="96bb4-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="96bb4-111">**Required/Optional**</span></span>|<span data-ttu-id="96bb4-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="96bb4-112">**Data Type**</span></span>|<span data-ttu-id="96bb4-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96bb4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96bb4-114">_сркангле_</span><span class="sxs-lookup"><span data-stu-id="96bb4-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="96bb4-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96bb4-115">Required</span></span>  <br/> |<span data-ttu-id="96bb4-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="96bb4-116">**Numeric**</span></span> <br/> |<span data-ttu-id="96bb4-117">Угол в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="96bb4-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="96bb4-118">_сркреф_</span><span class="sxs-lookup"><span data-stu-id="96bb4-118">_srcRef_</span></span> <br/> |<span data-ttu-id="96bb4-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96bb4-119">Required</span></span>  <br/> |<span data-ttu-id="96bb4-120">**String**</span><span class="sxs-lookup"><span data-stu-id="96bb4-120">**String**</span></span> <br/> | <span data-ttu-id="96bb4-121">Ссылка на ячейку в исходном объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="96bb4-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="96bb4-122">_дстреф_</span><span class="sxs-lookup"><span data-stu-id="96bb4-122">_dstRef_</span></span> <br/> |<span data-ttu-id="96bb4-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96bb4-123">Required</span></span>  <br/> |<span data-ttu-id="96bb4-124">**String**</span><span class="sxs-lookup"><span data-stu-id="96bb4-124">**String**</span></span> <br/> |<span data-ttu-id="96bb4-125">Ссылка на ячейку в целевом объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="96bb4-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96bb4-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="96bb4-126">Remarks</span></span>

<span data-ttu-id="96bb4-127">Функцию ANGLETOLOC можно использовать для установки локальных ячеек угла в фигуре с точки зрения угла из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="96bb4-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="96bb4-128">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="96bb4-128">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="96bb4-129">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="96bb4-129">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="96bb4-130">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="96bb4-130">The source and destination coordinates must be on the same page.</span></span>
  

