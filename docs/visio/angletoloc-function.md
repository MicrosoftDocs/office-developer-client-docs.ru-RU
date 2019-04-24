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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341477"
---
# <a name="angletoloc-function"></a><span data-ttu-id="8297f-104">Функция ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="8297f-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="8297f-105">Возвращает преобразованный угол в локальной системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="8297f-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="8297f-106">Преобразует угол из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="8297f-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8297f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8297f-107">Syntax</span></span>

<span data-ttu-id="8297f-108">ANGLETOLOC (\* \* *сркангле* \* \*, \* \* *сркреф* \* \*, \* \* *дстреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8297f-108">ANGLETOLOC(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8297f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8297f-109">Parameters</span></span>

|<span data-ttu-id="8297f-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8297f-110">**Name**</span></span>|<span data-ttu-id="8297f-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8297f-111">**Required/Optional**</span></span>|<span data-ttu-id="8297f-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8297f-112">**Data Type**</span></span>|<span data-ttu-id="8297f-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8297f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8297f-114">_Сркангле_</span><span class="sxs-lookup"><span data-stu-id="8297f-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="8297f-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8297f-115">Required</span></span>  <br/> |<span data-ttu-id="8297f-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8297f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="8297f-117">Угол в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="8297f-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="8297f-118">_Сркреф_</span><span class="sxs-lookup"><span data-stu-id="8297f-118">_srcRef_</span></span> <br/> |<span data-ttu-id="8297f-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8297f-119">Required</span></span>  <br/> |<span data-ttu-id="8297f-120">**String**</span><span class="sxs-lookup"><span data-stu-id="8297f-120">**String**</span></span> <br/> | <span data-ttu-id="8297f-121">Ссылка на ячейку в исходном объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="8297f-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="8297f-122">_Дстреф_</span><span class="sxs-lookup"><span data-stu-id="8297f-122">_dstRef_</span></span> <br/> |<span data-ttu-id="8297f-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8297f-123">Required</span></span>  <br/> |<span data-ttu-id="8297f-124">**String**</span><span class="sxs-lookup"><span data-stu-id="8297f-124">**String**</span></span> <br/> |<span data-ttu-id="8297f-125">Ссылка на ячейку в целевом объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="8297f-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8297f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8297f-126">Remarks</span></span>

<span data-ttu-id="8297f-127">Функцию ANGLETOLOC можно использовать для установки локальных ячеек угла в фигуре с точки зрения угла из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="8297f-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="8297f-128">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="8297f-128">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="8297f-129">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="8297f-129">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="8297f-130">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="8297f-130">The source and destination coordinates must be on the same page.</span></span>
  

