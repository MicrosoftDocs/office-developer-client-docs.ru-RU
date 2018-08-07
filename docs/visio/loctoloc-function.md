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
description: Возвращает преобразованную точку в локальной системе координат в конечной системе координат.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814181"
---
# <a name="loctoloc-function"></a><span data-ttu-id="2a4bb-103">Функция LOCTOLOC</span><span class="sxs-lookup"><span data-stu-id="2a4bb-103">LOCTOLOC Function</span></span>

<span data-ttu-id="2a4bb-104">Возвращает преобразованную точку в локальной системе координат в конечной системе координат.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2a4bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a4bb-105">Syntax</span></span>

<span data-ttu-id="2a4bb-106">LOCTOLOC (** *srcPoint* **, ** *srcRef* **, ** *dstRef* **)</span><span class="sxs-lookup"><span data-stu-id="2a4bb-106">LOCTOLOC(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2a4bb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a4bb-107">Parameters</span></span>

|<span data-ttu-id="2a4bb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-108">**Name**</span></span>|<span data-ttu-id="2a4bb-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-109">**Required/Optional**</span></span>|<span data-ttu-id="2a4bb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-110">**Data Type**</span></span>|<span data-ttu-id="2a4bb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2a4bb-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="2a4bb-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="2a4bb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2a4bb-113">Required</span></span>  <br/> |<span data-ttu-id="2a4bb-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-114">**String**</span></span> <br/> | <span data-ttu-id="2a4bb-115">Точка в локальной системе координат в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="2a4bb-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="2a4bb-116">_srcRef_</span></span> <br/> |<span data-ttu-id="2a4bb-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2a4bb-117">Required</span></span>  <br/> |<span data-ttu-id="2a4bb-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-118">**String**</span></span> <br/> | <span data-ttu-id="2a4bb-119">Ссылка на ячейку в объекте источника.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="2a4bb-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="2a4bb-120">_dstRef_</span></span> <br/> |<span data-ttu-id="2a4bb-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2a4bb-121">Required</span></span>  <br/> |<span data-ttu-id="2a4bb-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="2a4bb-122">**String**</span></span> <br/> | <span data-ttu-id="2a4bb-123">Ссылка на ячейку в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2a4bb-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="2a4bb-125">Строка</span><span class="sxs-lookup"><span data-stu-id="2a4bb-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a4bb-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a4bb-126">Remarks</span></span>

<span data-ttu-id="2a4bb-127">Функция LOCTOLOC преобразует точки из локальных координат исходной фигуры в локальные координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-127">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape.</span></span> <span data-ttu-id="2a4bb-128">Эта функция используется для создания фигуры, например, с точки зрения точка из другого пространства координат.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-128">You can use this function to construct a shape, for example, in terms of a point from another coordinate space.</span></span> <span data-ttu-id="2a4bb-129">Можно также использовать эту функцию для преобразования локального точки в координаты страницы или наоборот.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-129">You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="2a4bb-130">Эта функция работает даже в том случае, если исходный и целевой фигур, присутствующих в группах.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-130">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="2a4bb-131">Также настраивает для поворот и зеркальное отражение промежуточных преобразования.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-131">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="2a4bb-132">Координаты исходной и целевой должен находиться на той же странице.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="2a4bb-133">Пример</span><span class="sxs-lookup"><span data-stu-id="2a4bb-133">Example</span></span>

<span data-ttu-id="2a4bb-134">Следующая формула преобразует локальный ПИН-код фигуры, связанной с формулой момент на странице.</span><span class="sxs-lookup"><span data-stu-id="2a4bb-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


