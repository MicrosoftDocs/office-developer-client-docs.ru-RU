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
description: Возвращает преобразованную точку в родительских координатах в системе координат назначения.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439984"
---
# <a name="loctopar-function"></a><span data-ttu-id="56214-103">Функция LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="56214-103">LOCTOPAR Function</span></span>

<span data-ttu-id="56214-104">Возвращает преобразованную точку в родительских координатах в системе координат назначения.</span><span class="sxs-lookup"><span data-stu-id="56214-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="56214-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56214-105">Syntax</span></span>

<span data-ttu-id="56214-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="56214-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="56214-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="56214-107">Parameters</span></span>

|<span data-ttu-id="56214-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="56214-108">**Name**</span></span>|<span data-ttu-id="56214-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="56214-109">**Required/Optional**</span></span>|<span data-ttu-id="56214-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="56214-110">**Data Type**</span></span>|<span data-ttu-id="56214-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56214-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="56214-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="56214-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="56214-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56214-113">Required</span></span>  <br/> |<span data-ttu-id="56214-114">**String**</span><span class="sxs-lookup"><span data-stu-id="56214-114">**String**</span></span> <br/> | <span data-ttu-id="56214-115">Точка в локальных координатах в системе координат источника.</span><span class="sxs-lookup"><span data-stu-id="56214-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="56214-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="56214-116">_srcRef_</span></span> <br/> |<span data-ttu-id="56214-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56214-117">Required</span></span>  <br/> |<span data-ttu-id="56214-118">**String**</span><span class="sxs-lookup"><span data-stu-id="56214-118">**String**</span></span> <br/> | <span data-ttu-id="56214-119">Ссылка на ячейку в объекте источника.</span><span class="sxs-lookup"><span data-stu-id="56214-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="56214-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="56214-120">_dstRef_</span></span> <br/> |<span data-ttu-id="56214-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56214-121">Required</span></span>  <br/> |<span data-ttu-id="56214-122">**String**</span><span class="sxs-lookup"><span data-stu-id="56214-122">**String**</span></span> <br/> | <span data-ttu-id="56214-123">Ссылка на ячейку в объекте назначения.</span><span class="sxs-lookup"><span data-stu-id="56214-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="56214-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56214-124">Return value</span></span>

<span data-ttu-id="56214-125">String</span><span class="sxs-lookup"><span data-stu-id="56214-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56214-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="56214-126">Remarks</span></span>

<span data-ttu-id="56214-127">Преобразует точку из локальных координат в форме источника в родительские координаты в форме назначения.</span><span class="sxs-lookup"><span data-stu-id="56214-127">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape.</span></span> <span data-ttu-id="56214-128">Вы можете использовать функцию LOCTOPAR для набора родительских координат в ячейках, таких как PinX, PinY, BeginX и BeginY в форме, используя другую точку из другой системы координат.</span><span class="sxs-lookup"><span data-stu-id="56214-128">You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="56214-129">Эта функция работает даже в том случае, если исходные и назначения фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="56214-129">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="56214-130">Он также настраивается для вращения и сальто в промежуточной трансформации.</span><span class="sxs-lookup"><span data-stu-id="56214-130">It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="56214-131">Координаты источника и назначения должны быть на одной странице.</span><span class="sxs-lookup"><span data-stu-id="56214-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="56214-132">Если местом назначения является страница, не родительская, результат выражается в локальных координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="56214-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="56214-133">Пример</span><span class="sxs-lookup"><span data-stu-id="56214-133">Example</span></span>

<span data-ttu-id="56214-134">LOCTOPAR(PNT(LocPinX, LocPiny), Ширина, лист.4! Ширина)</span><span class="sxs-lookup"><span data-stu-id="56214-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="56214-135">Преобразует локальный пин-код фигуры, связанной с формулой, в родительские координаты Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="56214-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

