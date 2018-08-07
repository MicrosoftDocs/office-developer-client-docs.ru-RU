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
ms.openlocfilehash: 09ab0a4a55446dd74729f1da0bcf022d8376909b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813154"
---
# <a name="angletoloc-function"></a><span data-ttu-id="35a49-104">Функция ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="35a49-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="35a49-105">Возвращает преобразованный угол в локальной системе координат конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="35a49-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="35a49-106">Преобразует угол из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="35a49-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="35a49-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35a49-107">Syntax</span></span>

<span data-ttu-id="35a49-108">ANGLETOLOC (** *srcAngle* **, ** *srcRef* **, ** *dstRef* **)</span><span class="sxs-lookup"><span data-stu-id="35a49-108">ANGLETOLOC(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35a49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="35a49-109">Parameters</span></span>

|<span data-ttu-id="35a49-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="35a49-110">**Name**</span></span>|<span data-ttu-id="35a49-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="35a49-111">**Required/Optional**</span></span>|<span data-ttu-id="35a49-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="35a49-112">**Data Type**</span></span>|<span data-ttu-id="35a49-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35a49-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35a49-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="35a49-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="35a49-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35a49-115">Required</span></span>  <br/> |<span data-ttu-id="35a49-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="35a49-116">**Numeric**</span></span> <br/> |<span data-ttu-id="35a49-117">Угол в исходной системы координат.</span><span class="sxs-lookup"><span data-stu-id="35a49-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="35a49-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="35a49-118">_srcRef_</span></span> <br/> |<span data-ttu-id="35a49-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35a49-119">Required</span></span>  <br/> |<span data-ttu-id="35a49-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="35a49-120">**String**</span></span> <br/> | <span data-ttu-id="35a49-121">Ссылка на ячейку в объекте источника, например фигуры, группы, страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="35a49-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="35a49-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="35a49-122">_dstRef_</span></span> <br/> |<span data-ttu-id="35a49-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35a49-123">Required</span></span>  <br/> |<span data-ttu-id="35a49-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="35a49-124">**String**</span></span> <br/> |<span data-ttu-id="35a49-125">Ссылка на ячейку в целевой объект, например фигуры, группы, страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="35a49-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35a49-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="35a49-126">Remarks</span></span>

<span data-ttu-id="35a49-127">Функция ANGLETOLOC определения локальных ячеек угла в фигуре угла из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="35a49-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="35a49-128">Эта функция работает даже в том случае, если исходный и целевой фигур, присутствующих в группах.</span><span class="sxs-lookup"><span data-stu-id="35a49-128">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="35a49-129">Также настраивает для поворот и зеркальное отражение промежуточных преобразования.</span><span class="sxs-lookup"><span data-stu-id="35a49-129">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="35a49-130">Координаты исходной и целевой должен находиться на той же странице.</span><span class="sxs-lookup"><span data-stu-id="35a49-130">The source and destination coordinates must be on the same page.</span></span>
  

