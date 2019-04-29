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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421545"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="c6d6a-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c6d6a-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c6d6a-105">Возвращает значение TRUE, если значение _целлреференце_ имеет любой тип ошибки; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="c6d6a-106">Функция ЕОШИБКА используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6d6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6d6a-107">Syntax</span></span>

<span data-ttu-id="c6d6a-108">Ошибка (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c6d6a-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6d6a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6d6a-109">Parameters</span></span>

|<span data-ttu-id="c6d6a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-110">**Name**</span></span>|<span data-ttu-id="c6d6a-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-111">**Required/Optional**</span></span>|<span data-ttu-id="c6d6a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-112">**Data Type**</span></span>|<span data-ttu-id="c6d6a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6d6a-114">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="c6d6a-114">_cellreference_</span></span> <br/> |<span data-ttu-id="c6d6a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6d6a-115">Required</span></span>  <br/> |<span data-ttu-id="c6d6a-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-116">**String**</span></span> <br/> |<span data-ttu-id="c6d6a-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="c6d6a-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6d6a-118">Example 1</span></span>

|<span data-ttu-id="c6d6a-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-119">**Cell**</span></span>|<span data-ttu-id="c6d6a-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-120">**Formula**</span></span>|<span data-ttu-id="c6d6a-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c6d6a-122">". A1"</span><span class="sxs-lookup"><span data-stu-id="c6d6a-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="c6d6a-123">= НД ()</span><span class="sxs-lookup"><span data-stu-id="c6d6a-123">=NA( )</span></span>  <br/> |<span data-ttu-id="c6d6a-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="c6d6a-125">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="c6d6a-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="c6d6a-126">= Ошибка (". a1")</span><span class="sxs-lookup"><span data-stu-id="c6d6a-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="c6d6a-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6d6a-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="c6d6a-128">Возвращает значение TRUE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-128">Returns TRUE because the #N/A!</span></span> <span data-ttu-id="c6d6a-129">Ошибка распознается функцией ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-129">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="c6d6a-130">Вы можете использовать ЕОШ для поиска всех типов, но #N/A!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-130">You can use ISERR to find all types but the #N/A!</span></span> <span data-ttu-id="c6d6a-131">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-131">error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c6d6a-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c6d6a-132">Example 2</span></span>

|<span data-ttu-id="c6d6a-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-133">**Cell**</span></span>|<span data-ttu-id="c6d6a-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-134">**Formula**</span></span>|<span data-ttu-id="c6d6a-135">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="c6d6a-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c6d6a-136">"С начала. x1"</span><span class="sxs-lookup"><span data-stu-id="c6d6a-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="c6d6a-137">= "Дом"</span><span class="sxs-lookup"><span data-stu-id="c6d6a-137">="House"</span></span>  <br/> |<span data-ttu-id="c6d6a-138">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="c6d6a-139">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="c6d6a-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="c6d6a-140">= Ошибка (". x1)"</span><span class="sxs-lookup"><span data-stu-id="c6d6a-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="c6d6a-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6d6a-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="c6d6a-142">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-142">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="c6d6a-143">Ошибка распознается функцией ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-143">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="c6d6a-144">Создание выражения на основе #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c6d6a-144">To build an expression based on the #VALUE!</span></span> <span data-ttu-id="c6d6a-145">ошибка, используйте функцию ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="c6d6a-145">error, use the ISERRVALUE function.</span></span>
  

