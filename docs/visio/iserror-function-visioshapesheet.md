---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Возвращает значение TRUE, если значение ссылка_на_ячейку имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ISERROR используется в формулах, которые ссылаются на другую ячейку.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813997"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="6869d-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6869d-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6869d-105">Возвращает значение TRUE, если значение _ссылка_на_ячейку_ имеет любой тип ошибки; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="6869d-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="6869d-106">Функция ISERROR используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="6869d-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6869d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6869d-107">Syntax</span></span>

<span data-ttu-id="6869d-108">ЕОШИБКА (** *ссылка_на_ячейку* **)</span><span class="sxs-lookup"><span data-stu-id="6869d-108">ISERROR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6869d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6869d-109">Parameters</span></span>

|<span data-ttu-id="6869d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6869d-110">**Name**</span></span>|<span data-ttu-id="6869d-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6869d-111">**Required/Optional**</span></span>|<span data-ttu-id="6869d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6869d-112">**Data Type**</span></span>|<span data-ttu-id="6869d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6869d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6869d-114">_ссылка_на_ячейку_</span><span class="sxs-lookup"><span data-stu-id="6869d-114">_cellreference_</span></span> <br/> |<span data-ttu-id="6869d-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6869d-115">Required</span></span>  <br/> |<span data-ttu-id="6869d-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6869d-116">**String**</span></span> <br/> |<span data-ttu-id="6869d-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="6869d-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="6869d-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6869d-118">Example 1</span></span>

|<span data-ttu-id="6869d-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6869d-119">**Cell**</span></span>|<span data-ttu-id="6869d-120">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="6869d-120">**Formula**</span></span>|<span data-ttu-id="6869d-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="6869d-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6869d-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="6869d-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="6869d-123">= (НД)</span><span class="sxs-lookup"><span data-stu-id="6869d-123">=NA( )</span></span>  <br/> |<span data-ttu-id="6869d-124"># Н/Д!</span><span class="sxs-lookup"><span data-stu-id="6869d-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="6869d-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="6869d-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="6869d-126">=ISERROR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="6869d-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="6869d-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="6869d-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="6869d-128">Возвращает значение TRUE, так как # н/д!</span><span class="sxs-lookup"><span data-stu-id="6869d-128">Returns TRUE because the #N/A!</span></span> <span data-ttu-id="6869d-129">Ошибка распознается функцию ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="6869d-129">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="6869d-130">ЕОШ можно использовать для поиска всех типов, но # н/д!</span><span class="sxs-lookup"><span data-stu-id="6869d-130">You can use ISERR to find all types but the #N/A!</span></span> <span data-ttu-id="6869d-131">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="6869d-131">error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6869d-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6869d-132">Example 2</span></span>

|<span data-ttu-id="6869d-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6869d-133">**Cell**</span></span>|<span data-ttu-id="6869d-134">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="6869d-134">**Formula**</span></span>|<span data-ttu-id="6869d-135">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="6869d-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6869d-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="6869d-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="6869d-137">= «Дом»</span><span class="sxs-lookup"><span data-stu-id="6869d-137">="House"</span></span>  <br/> |<span data-ttu-id="6869d-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="6869d-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="6869d-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="6869d-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="6869d-140">=ISERROR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="6869d-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="6869d-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="6869d-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="6869d-142">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6869d-142">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="6869d-143">Ошибка распознается функцию ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="6869d-143">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="6869d-144">Для построения выражения на основании #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6869d-144">To build an expression based on the #VALUE!</span></span> <span data-ttu-id="6869d-145">Ошибка, используйте функцию ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="6869d-145">error, use the ISERRVALUE function.</span></span>
  

