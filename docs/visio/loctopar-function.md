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
description: Возвращает преобразованную точку в родительских координат в конечной системе координат.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814190"
---
# <a name="loctopar-function"></a><span data-ttu-id="f0b61-103">Функция LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="f0b61-103">LOCTOPAR Function</span></span>

<span data-ttu-id="f0b61-104">Возвращает преобразованную точку в родительских координат в конечной системе координат.</span><span class="sxs-lookup"><span data-stu-id="f0b61-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f0b61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0b61-105">Syntax</span></span>

<span data-ttu-id="f0b61-106">LOCTOPAR (** *srcPoint* **, ** *srcRef* **, ** *dstRef* **)</span><span class="sxs-lookup"><span data-stu-id="f0b61-106">LOCTOPAR(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f0b61-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0b61-107">Parameters</span></span>

|<span data-ttu-id="f0b61-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f0b61-108">**Name**</span></span>|<span data-ttu-id="f0b61-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f0b61-109">**Required/Optional**</span></span>|<span data-ttu-id="f0b61-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f0b61-110">**Data Type**</span></span>|<span data-ttu-id="f0b61-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0b61-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f0b61-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="f0b61-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="f0b61-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0b61-113">Required</span></span>  <br/> |<span data-ttu-id="f0b61-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f0b61-114">**String**</span></span> <br/> | <span data-ttu-id="f0b61-115">Точка в локальной системе координат в исходной системе координат.</span><span class="sxs-lookup"><span data-stu-id="f0b61-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="f0b61-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="f0b61-116">_srcRef_</span></span> <br/> |<span data-ttu-id="f0b61-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0b61-117">Required</span></span>  <br/> |<span data-ttu-id="f0b61-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f0b61-118">**String**</span></span> <br/> | <span data-ttu-id="f0b61-119">Ссылка на ячейку в объекте источника.</span><span class="sxs-lookup"><span data-stu-id="f0b61-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="f0b61-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="f0b61-120">_dstRef_</span></span> <br/> |<span data-ttu-id="f0b61-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f0b61-121">Required</span></span>  <br/> |<span data-ttu-id="f0b61-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f0b61-122">**String**</span></span> <br/> | <span data-ttu-id="f0b61-123">Ссылка на ячейку в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="f0b61-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f0b61-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f0b61-124">Return value</span></span>

<span data-ttu-id="f0b61-125">Строка</span><span class="sxs-lookup"><span data-stu-id="f0b61-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0b61-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0b61-126">Remarks</span></span>

<span data-ttu-id="f0b61-127">Преобразует точки из локальных координат исходной фигуры в родительские координаты конечной фигуры.</span><span class="sxs-lookup"><span data-stu-id="f0b61-127">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape.</span></span> <span data-ttu-id="f0b61-128">Функция LOCTOPAR позволяет задать координаты родительского в ячейках, такие как PinX, PinY, BeginX и BeginY использование другой точки из другой системы координат фигуры.</span><span class="sxs-lookup"><span data-stu-id="f0b61-128">You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="f0b61-129">Эта функция работает даже в том случае, если исходный и целевой фигур, присутствующих в группах.</span><span class="sxs-lookup"><span data-stu-id="f0b61-129">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="f0b61-130">Также настраивает для поворот и зеркальное отражение промежуточных преобразования.</span><span class="sxs-lookup"><span data-stu-id="f0b61-130">It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="f0b61-131">Координаты исходной и целевой должен находиться на той же странице.</span><span class="sxs-lookup"><span data-stu-id="f0b61-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="f0b61-132">Если destination является страницу, которая не имеет родительского, результат выражается в локальной системе координат страницы.</span><span class="sxs-lookup"><span data-stu-id="f0b61-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f0b61-133">Пример</span><span class="sxs-lookup"><span data-stu-id="f0b61-133">Example</span></span>

<span data-ttu-id="f0b61-134">LOCTOPAR (раздела PNT (LocPinX, LocPinY), Width, Sheet.4! Ширина)</span><span class="sxs-lookup"><span data-stu-id="f0b61-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="f0b61-135">Преобразует локальный ПИН-код фигуры, связанной с формулу для родительского координаты Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="f0b61-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

