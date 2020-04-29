---
title: Функция ISERRNA
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Возвращает значение TRUE, если значение целлреференце имеет тип ошибки #N/A! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432116"
---
# <a name="iserrna-function"></a><span data-ttu-id="fe053-105">Функция ISERRNA</span><span class="sxs-lookup"><span data-stu-id="fe053-105">ISERRNA Function</span></span>

<span data-ttu-id="fe053-106">Возвращает значение TRUE, если значение _целлреференце_ имеет тип ошибки #N/a!</span><span class="sxs-lookup"><span data-stu-id="fe053-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="fe053-107">(недоступно); в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="fe053-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="fe053-108">Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="fe053-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fe053-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe053-109">Syntax</span></span>

<span data-ttu-id="fe053-110">ISERRNA (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fe053-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe053-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe053-111">Parameters</span></span>

|<span data-ttu-id="fe053-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fe053-112">**Name**</span></span>|<span data-ttu-id="fe053-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fe053-113">**Required/Optional**</span></span>|<span data-ttu-id="fe053-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fe053-114">**Data Type**</span></span>|<span data-ttu-id="fe053-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe053-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe053-116">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="fe053-116">_cellreference_</span></span> <br/> |<span data-ttu-id="fe053-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fe053-117">Required</span></span>  <br/> |<span data-ttu-id="fe053-118">**String**</span><span class="sxs-lookup"><span data-stu-id="fe053-118">**String**</span></span> <br/> |<span data-ttu-id="fe053-119">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="fe053-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="fe053-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe053-120">Example 1</span></span>

|<span data-ttu-id="fe053-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fe053-121">**Cell**</span></span>|<span data-ttu-id="fe053-122">**Формула**</span><span class="sxs-lookup"><span data-stu-id="fe053-122">**Formula**</span></span>|<span data-ttu-id="fe053-123">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="fe053-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe053-124">". A1"</span><span class="sxs-lookup"><span data-stu-id="fe053-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="fe053-125">= "5 + 3"</span><span class="sxs-lookup"><span data-stu-id="fe053-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="fe053-126">8,5</span><span class="sxs-lookup"><span data-stu-id="fe053-126">"8"</span></span>  <br/> |
|<span data-ttu-id="fe053-127">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="fe053-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fe053-128">= ISERRNA ("a. a1")</span><span class="sxs-lookup"><span data-stu-id="fe053-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="fe053-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="fe053-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="fe053-130">Возвращает значение FALSE, так как возвращаемое значение доступно.</span><span class="sxs-lookup"><span data-stu-id="fe053-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fe053-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe053-131">Example 2</span></span>

|<span data-ttu-id="fe053-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fe053-132">**Cell**</span></span>|<span data-ttu-id="fe053-133">**Формула**</span><span class="sxs-lookup"><span data-stu-id="fe053-133">**Formula**</span></span>|<span data-ttu-id="fe053-134">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="fe053-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe053-135">". A1"</span><span class="sxs-lookup"><span data-stu-id="fe053-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="fe053-136">= НД ()</span><span class="sxs-lookup"><span data-stu-id="fe053-136">=NA( )</span></span>  <br/> |<span data-ttu-id="fe053-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="fe053-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="fe053-138">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="fe053-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fe053-139">= ISERRNA ("a. a1")</span><span class="sxs-lookup"><span data-stu-id="fe053-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="fe053-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="fe053-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="fe053-141">Возвращает значение TRUE, так как возвращаемое значение имеет тип ошибки #N/A!</span><span class="sxs-lookup"><span data-stu-id="fe053-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

