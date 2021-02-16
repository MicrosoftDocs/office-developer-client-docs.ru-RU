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
description: Возвращает преобразованный угол в родительской системе координат фигуры назначения. Преобразует угол из локальных координат в форме источника в родительские координаты в фигуре назначения.
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160260"
---
# <a name="angletopar-function"></a><span data-ttu-id="095e8-104">Функция ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="095e8-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="095e8-105">Возвращает преобразованный угол в родительской системе координат фигуры назначения.</span><span class="sxs-lookup"><span data-stu-id="095e8-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="095e8-106">Преобразует угол из локальных координат в форме источника в родительские координаты в фигуре назначения.</span><span class="sxs-lookup"><span data-stu-id="095e8-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="095e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="095e8-107">Syntax</span></span>

<span data-ttu-id="095e8-108">ANGLETOPAR(***srcAngle,*** ***srcRef***, ***dstRef*** )</span><span class="sxs-lookup"><span data-stu-id="095e8-108">ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="095e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="095e8-109">Parameters</span></span>

|<span data-ttu-id="095e8-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="095e8-110">**Name**</span></span>|<span data-ttu-id="095e8-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="095e8-111">**Required/Optional**</span></span>|<span data-ttu-id="095e8-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="095e8-112">**Data Type**</span></span>|<span data-ttu-id="095e8-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="095e8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="095e8-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="095e8-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="095e8-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="095e8-115">Required</span></span>  <br/> |<span data-ttu-id="095e8-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="095e8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="095e8-117">Угол в системе координат источника.</span><span class="sxs-lookup"><span data-stu-id="095e8-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="095e8-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="095e8-118">_srcRef_</span></span> <br/> |<span data-ttu-id="095e8-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="095e8-119">Required</span></span>  <br/> |<span data-ttu-id="095e8-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="095e8-120">**String**</span></span> <br/> | <span data-ttu-id="095e8-121">Ссылка на ячейку в объекте-источнике, например фигуру, группу, страницу и так далее.</span><span class="sxs-lookup"><span data-stu-id="095e8-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="095e8-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="095e8-122">_dstRef_</span></span> <br/> |<span data-ttu-id="095e8-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="095e8-123">Required</span></span>  <br/> |<span data-ttu-id="095e8-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="095e8-124">**String**</span></span> <br/> |<span data-ttu-id="095e8-125">Ссылка на ячейку в объекте назначения, например фигуру, группу, страницу и так далее.</span><span class="sxs-lookup"><span data-stu-id="095e8-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="095e8-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="095e8-126">Remarks</span></span>

<span data-ttu-id="095e8-127">Эта функция работает, даже если исходные и пунктов назначения фигуры находятся в группах.</span><span class="sxs-lookup"><span data-stu-id="095e8-127">This function works even when the source and destination shapes are within groups.</span></span> <span data-ttu-id="095e8-128">Он также настраивается для поворота и пролистывок в промежуточном преобразовании.</span><span class="sxs-lookup"><span data-stu-id="095e8-128">It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="095e8-129">Координаты источника и назначения должны быть на одной странице.</span><span class="sxs-lookup"><span data-stu-id="095e8-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="095e8-130">Если местом назначения является страница без родительского сайта, результат выражается в локальных координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="095e8-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

