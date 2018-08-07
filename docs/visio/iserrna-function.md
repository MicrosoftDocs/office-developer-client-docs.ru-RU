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
description: 'Возвращает значение TRUE, если значение ссылка_на_ячейку имеет тип ошибки, # н/д! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813995"
---
# <a name="iserrna-function"></a><span data-ttu-id="1c559-105">Функция ISERRNA</span><span class="sxs-lookup"><span data-stu-id="1c559-105">ISERRNA Function</span></span>

<span data-ttu-id="1c559-106">Возвращает значение TRUE, если значение _ссылка_на_ячейку_ имеет тип ошибки, # н/д!</span><span class="sxs-lookup"><span data-stu-id="1c559-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="1c559-107">(недоступно); в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="1c559-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="1c559-108">Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="1c559-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1c559-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c559-109">Syntax</span></span>

<span data-ttu-id="1c559-110">ISERRNA (** *ссылка_на_ячейку* **)</span><span class="sxs-lookup"><span data-stu-id="1c559-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1c559-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c559-111">Parameters</span></span>

|<span data-ttu-id="1c559-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1c559-112">**Name**</span></span>|<span data-ttu-id="1c559-113">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="1c559-113">**Required/Optional**</span></span>|<span data-ttu-id="1c559-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1c559-114">**Data Type**</span></span>|<span data-ttu-id="1c559-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c559-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1c559-116">_ссылка_на_ячейку_</span><span class="sxs-lookup"><span data-stu-id="1c559-116">_cellreference_</span></span> <br/> |<span data-ttu-id="1c559-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1c559-117">Required</span></span>  <br/> |<span data-ttu-id="1c559-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="1c559-118">**String**</span></span> <br/> |<span data-ttu-id="1c559-119">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="1c559-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="1c559-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c559-120">Example 1</span></span>

|<span data-ttu-id="1c559-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1c559-121">**Cell**</span></span>|<span data-ttu-id="1c559-122">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="1c559-122">**Formula**</span></span>|<span data-ttu-id="1c559-123">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="1c559-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c559-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="1c559-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1c559-125">= «5 + 3»</span><span class="sxs-lookup"><span data-stu-id="1c559-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="1c559-126">«8»</span><span class="sxs-lookup"><span data-stu-id="1c559-126">"8"</span></span>  <br/> |
|<span data-ttu-id="1c559-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="1c559-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1c559-128">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="1c559-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1c559-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="1c559-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="1c559-130">Возвращает значение FALSE, так как значение, возвращаемое доступен.</span><span class="sxs-lookup"><span data-stu-id="1c559-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1c559-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c559-131">Example 2</span></span>

|<span data-ttu-id="1c559-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1c559-132">**Cell**</span></span>|<span data-ttu-id="1c559-133">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="1c559-133">**Formula**</span></span>|<span data-ttu-id="1c559-134">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="1c559-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c559-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="1c559-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1c559-136">= (НД)</span><span class="sxs-lookup"><span data-stu-id="1c559-136">=NA( )</span></span>  <br/> |<span data-ttu-id="1c559-137"># Н/Д!</span><span class="sxs-lookup"><span data-stu-id="1c559-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="1c559-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="1c559-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1c559-139">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="1c559-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1c559-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="1c559-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="1c559-141">Возвращает TRUE, так как возвращаемое значение Ошибка типа # н/д!</span><span class="sxs-lookup"><span data-stu-id="1c559-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

