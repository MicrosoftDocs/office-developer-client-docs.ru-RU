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
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433572"
---
# <a name="angletoloc-function"></a><span data-ttu-id="cca7c-104">Функция ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="cca7c-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="cca7c-105">Возвращает преобразованный угол в локальной системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="cca7c-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="cca7c-106">Преобразует угол из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="cca7c-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cca7c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cca7c-107">Syntax</span></span>

<span data-ttu-id="cca7c-108">ANGLETOLOC (\* \* *сркангле* \* \*, \* \* *сркреф* \* \*, \* \* *дстреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cca7c-108">ANGLETOLOC(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cca7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cca7c-109">Parameters</span></span>

|<span data-ttu-id="cca7c-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cca7c-110">**Name**</span></span>|<span data-ttu-id="cca7c-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="cca7c-111">**Required/Optional**</span></span>|<span data-ttu-id="cca7c-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cca7c-112">**Data Type**</span></span>|<span data-ttu-id="cca7c-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cca7c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cca7c-114">_сркангле_</span><span class="sxs-lookup"><span data-stu-id="cca7c-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="cca7c-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="cca7c-115">Required</span></span>  <br/> |<span data-ttu-id="cca7c-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="cca7c-116">**Numeric**</span></span> <br/> |<span data-ttu-id="cca7c-117">Угол в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="cca7c-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="cca7c-118">_сркреф_</span><span class="sxs-lookup"><span data-stu-id="cca7c-118">_srcRef_</span></span> <br/> |<span data-ttu-id="cca7c-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cca7c-119">Required</span></span>  <br/> |<span data-ttu-id="cca7c-120">**String**</span><span class="sxs-lookup"><span data-stu-id="cca7c-120">**String**</span></span> <br/> | <span data-ttu-id="cca7c-121">Ссылка на ячейку в исходном объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="cca7c-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="cca7c-122">_дстреф_</span><span class="sxs-lookup"><span data-stu-id="cca7c-122">_dstRef_</span></span> <br/> |<span data-ttu-id="cca7c-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cca7c-123">Required</span></span>  <br/> |<span data-ttu-id="cca7c-124">**String**</span><span class="sxs-lookup"><span data-stu-id="cca7c-124">**String**</span></span> <br/> |<span data-ttu-id="cca7c-125">Ссылка на ячейку в целевом объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="cca7c-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cca7c-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="cca7c-126">Remarks</span></span>

<span data-ttu-id="cca7c-127">Функцию ANGLETOLOC можно использовать для установки локальных ячеек угла в фигуре с точки зрения угла из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="cca7c-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="cca7c-128">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="cca7c-128">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="cca7c-129">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="cca7c-129">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="cca7c-130">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="cca7c-130">The source and destination coordinates must be on the same page.</span></span>
  

