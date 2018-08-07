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
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813162"
---
# <a name="angletopar-function"></a><span data-ttu-id="47e79-104">Функция ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="47e79-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="47e79-105">Возвращает преобразованный угол в родительской системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="47e79-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="47e79-106">Преобразует угол из локальных координат исходной фигуры в родительские координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="47e79-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="47e79-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47e79-107">Syntax</span></span>

<span data-ttu-id="47e79-108">ANGLETOPAR (** *srcAngle* **, ** *srcRef* **, ** *dstRef* **)</span><span class="sxs-lookup"><span data-stu-id="47e79-108">ANGLETOPAR(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="47e79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="47e79-109">Parameters</span></span>

|<span data-ttu-id="47e79-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="47e79-110">**Name**</span></span>|<span data-ttu-id="47e79-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="47e79-111">**Required/Optional**</span></span>|<span data-ttu-id="47e79-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="47e79-112">**Data Type**</span></span>|<span data-ttu-id="47e79-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47e79-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="47e79-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="47e79-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="47e79-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="47e79-115">Required</span></span>  <br/> |<span data-ttu-id="47e79-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="47e79-116">**Numeric**</span></span> <br/> |<span data-ttu-id="47e79-117">Угол в исходной системы координат.</span><span class="sxs-lookup"><span data-stu-id="47e79-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="47e79-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="47e79-118">_srcRef_</span></span> <br/> |<span data-ttu-id="47e79-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="47e79-119">Required</span></span>  <br/> |<span data-ttu-id="47e79-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="47e79-120">**String**</span></span> <br/> | <span data-ttu-id="47e79-121">Ссылка на ячейку в объекте источника, например фигуры, группы, страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="47e79-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="47e79-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="47e79-122">_dstRef_</span></span> <br/> |<span data-ttu-id="47e79-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="47e79-123">Required</span></span>  <br/> |<span data-ttu-id="47e79-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="47e79-124">**String**</span></span> <br/> |<span data-ttu-id="47e79-125">Ссылка на ячейку в целевой объект, например фигуры, группы, страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="47e79-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47e79-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="47e79-126">Remarks</span></span>

<span data-ttu-id="47e79-127">Эта функция работает даже в том случае, если исходный и целевой фигур, присутствующих в группах.</span><span class="sxs-lookup"><span data-stu-id="47e79-127">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="47e79-128">Также настраивает для поворот и зеркальное отражение промежуточных преобразования.</span><span class="sxs-lookup"><span data-stu-id="47e79-128">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="47e79-129">Координаты исходной и целевой должен находиться на той же странице.</span><span class="sxs-lookup"><span data-stu-id="47e79-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="47e79-130">Если destination является страницу, которая не имеет родительского, результат выражается в локальной системе координат страницы.</span><span class="sxs-lookup"><span data-stu-id="47e79-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

