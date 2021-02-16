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
description: Возвращает преобразованный угол в локальной системе координат фигуры назначения. Преобразует угол из локальных координат в форме источника в локальные координаты в фигуре назначения.
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160267"
---
# <a name="angletoloc-function"></a><span data-ttu-id="43b9d-104">Функция ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="43b9d-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="43b9d-105">Возвращает преобразованный угол в локальной системе координат фигуры назначения.</span><span class="sxs-lookup"><span data-stu-id="43b9d-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="43b9d-106">Преобразует угол из локальных координат в форме источника в локальные координаты в фигуре назначения.</span><span class="sxs-lookup"><span data-stu-id="43b9d-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="43b9d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43b9d-107">Syntax</span></span>

<span data-ttu-id="43b9d-108">ANGLETOLOC(***srcAngle,*** ***srcRef***, ***dstRef*** )</span><span class="sxs-lookup"><span data-stu-id="43b9d-108">ANGLETOLOC(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43b9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43b9d-109">Parameters</span></span>

|<span data-ttu-id="43b9d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="43b9d-110">**Name**</span></span>|<span data-ttu-id="43b9d-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="43b9d-111">**Required/Optional**</span></span>|<span data-ttu-id="43b9d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="43b9d-112">**Data Type**</span></span>|<span data-ttu-id="43b9d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43b9d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43b9d-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="43b9d-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="43b9d-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="43b9d-115">Required</span></span>  <br/> |<span data-ttu-id="43b9d-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="43b9d-116">**Numeric**</span></span> <br/> |<span data-ttu-id="43b9d-117">Угол в системе координат источника.</span><span class="sxs-lookup"><span data-stu-id="43b9d-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="43b9d-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="43b9d-118">_srcRef_</span></span> <br/> |<span data-ttu-id="43b9d-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43b9d-119">Required</span></span>  <br/> |<span data-ttu-id="43b9d-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="43b9d-120">**String**</span></span> <br/> | <span data-ttu-id="43b9d-121">Ссылка на ячейку в объекте-источнике, например фигуру, группу, страницу и так далее.</span><span class="sxs-lookup"><span data-stu-id="43b9d-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="43b9d-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="43b9d-122">_dstRef_</span></span> <br/> |<span data-ttu-id="43b9d-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43b9d-123">Required</span></span>  <br/> |<span data-ttu-id="43b9d-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="43b9d-124">**String**</span></span> <br/> |<span data-ttu-id="43b9d-125">Ссылка на ячейку в объекте назначения, например фигуру, группу, страницу и так далее.</span><span class="sxs-lookup"><span data-stu-id="43b9d-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43b9d-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="43b9d-126">Remarks</span></span>

<span data-ttu-id="43b9d-127">Вы можете использовать функцию ANGLETOLOC, чтобы установить локальные угловые ячейки в фигуре с точки зрения угла из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="43b9d-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="43b9d-128">Эта функция работает, даже если исходные и пунктов назначения фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="43b9d-128">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="43b9d-129">Он также настраивается для поворота и пролистывок в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="43b9d-129">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="43b9d-130">Координаты источника и назначения должны быть на одной странице.</span><span class="sxs-lookup"><span data-stu-id="43b9d-130">The source and destination coordinates must be on the same page.</span></span>
  

