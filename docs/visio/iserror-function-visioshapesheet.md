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
description: Возвращает значение TRUE, если значение целлреференце имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ЕОШИБКА используется в формулах, которые ссылаются на другую ячейку.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317894"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="69310-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="69310-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="69310-105">Возвращает значение TRUE, если значение _целлреференце_ имеет любой тип ошибки; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="69310-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="69310-106">Функция ЕОШИБКА используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="69310-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="69310-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69310-107">Syntax</span></span>

<span data-ttu-id="69310-108">Ошибка (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="69310-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="69310-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="69310-109">Parameters</span></span>

|<span data-ttu-id="69310-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="69310-110">**Name**</span></span>|<span data-ttu-id="69310-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="69310-111">**Required/Optional**</span></span>|<span data-ttu-id="69310-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="69310-112">**Data Type**</span></span>|<span data-ttu-id="69310-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="69310-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="69310-114">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="69310-114">_cellreference_</span></span> <br/> |<span data-ttu-id="69310-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="69310-115">Required</span></span>  <br/> |<span data-ttu-id="69310-116">**String**</span><span class="sxs-lookup"><span data-stu-id="69310-116">**String**</span></span> <br/> |<span data-ttu-id="69310-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="69310-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="69310-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69310-118">Example 1</span></span>

|<span data-ttu-id="69310-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="69310-119">**Cell**</span></span>|<span data-ttu-id="69310-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="69310-120">**Formula**</span></span>|<span data-ttu-id="69310-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="69310-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69310-122">". A1"</span><span class="sxs-lookup"><span data-stu-id="69310-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="69310-123">= НД ()</span><span class="sxs-lookup"><span data-stu-id="69310-123">=NA( )</span></span>  <br/> |<span data-ttu-id="69310-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="69310-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="69310-125">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="69310-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="69310-126">= Ошибка (". a1")</span><span class="sxs-lookup"><span data-stu-id="69310-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="69310-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="69310-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="69310-128">Возвращает значение TRUE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="69310-128">Returns TRUE because the #N/A!</span></span> <span data-ttu-id="69310-129">Ошибка распознается функцией ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="69310-129">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="69310-130">Вы можете использовать ЕОШ для поиска всех типов, но #N/A!</span><span class="sxs-lookup"><span data-stu-id="69310-130">You can use ISERR to find all types but the #N/A!</span></span> <span data-ttu-id="69310-131">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="69310-131">error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="69310-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69310-132">Example 2</span></span>

|<span data-ttu-id="69310-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="69310-133">**Cell**</span></span>|<span data-ttu-id="69310-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="69310-134">**Formula**</span></span>|<span data-ttu-id="69310-135">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="69310-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69310-136">"С начала. x1"</span><span class="sxs-lookup"><span data-stu-id="69310-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="69310-137">= "Дом"</span><span class="sxs-lookup"><span data-stu-id="69310-137">="House"</span></span>  <br/> |<span data-ttu-id="69310-138">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="69310-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="69310-139">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="69310-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="69310-140">= Ошибка (". x1)"</span><span class="sxs-lookup"><span data-stu-id="69310-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="69310-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="69310-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="69310-142">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="69310-142">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="69310-143">Ошибка распознается функцией ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="69310-143">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="69310-144">Создание выражения на основе #VALUE!</span><span class="sxs-lookup"><span data-stu-id="69310-144">To build an expression based on the #VALUE!</span></span> <span data-ttu-id="69310-145">ошибка, используйте функцию ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="69310-145">error, use the ISERRVALUE function.</span></span>
  

