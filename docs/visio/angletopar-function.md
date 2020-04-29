---
title: Функция ANGLETOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Возвращает преобразованный угол в родительской системе координат конечной фигуры. Преобразует угол из локальных координат исходной фигуры в родительские координаты конечной фигуры.
ms.openlocfilehash: e411cbae21d832039e2fbda93393a8fe0bd1f9f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404325"
---
# <a name="angletopar-function"></a><span data-ttu-id="e2ec8-104">Функция ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="e2ec8-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="e2ec8-105">Возвращает преобразованный угол в родительской системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="e2ec8-106">Преобразует угол из локальных координат исходной фигуры в родительские координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e2ec8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2ec8-107">Syntax</span></span>

<span data-ttu-id="e2ec8-108">ANGLETOPAR (\* \* *сркангле* \* \*, \* \* *сркреф* \* \*, \* \* *дстреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e2ec8-108">ANGLETOPAR(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e2ec8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2ec8-109">Parameters</span></span>

|<span data-ttu-id="e2ec8-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-110">**Name**</span></span>|<span data-ttu-id="e2ec8-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-111">**Required/Optional**</span></span>|<span data-ttu-id="e2ec8-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-112">**Data Type**</span></span>|<span data-ttu-id="e2ec8-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e2ec8-114">_сркангле_</span><span class="sxs-lookup"><span data-stu-id="e2ec8-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="e2ec8-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e2ec8-115">Required</span></span>  <br/> |<span data-ttu-id="e2ec8-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e2ec8-117">Угол в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="e2ec8-118">_сркреф_</span><span class="sxs-lookup"><span data-stu-id="e2ec8-118">_srcRef_</span></span> <br/> |<span data-ttu-id="e2ec8-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e2ec8-119">Required</span></span>  <br/> |<span data-ttu-id="e2ec8-120">**String**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-120">**String**</span></span> <br/> | <span data-ttu-id="e2ec8-121">Ссылка на ячейку в исходном объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="e2ec8-122">_дстреф_</span><span class="sxs-lookup"><span data-stu-id="e2ec8-122">_dstRef_</span></span> <br/> |<span data-ttu-id="e2ec8-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e2ec8-123">Required</span></span>  <br/> |<span data-ttu-id="e2ec8-124">**String**</span><span class="sxs-lookup"><span data-stu-id="e2ec8-124">**String**</span></span> <br/> |<span data-ttu-id="e2ec8-125">Ссылка на ячейку в целевом объекте, например фигуру, группу, страницу и т. д.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2ec8-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2ec8-126">Remarks</span></span>

<span data-ttu-id="e2ec8-127">Эта функция работает, даже если исходная и конечная фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-127">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="e2ec8-128">Он также настраивается для вращения и отражения в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-128">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="e2ec8-129">Координаты источника и назначения должны находиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="e2ec8-130">Если объект Destination является страницей, не имеющей родителя, результат выражается в локальных координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="e2ec8-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

