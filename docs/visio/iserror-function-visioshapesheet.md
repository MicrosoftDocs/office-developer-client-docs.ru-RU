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
description: Возвращает значение TRUE, если значение cellreference имеет какой-либо тип ошибки; в противном случае возвращается false. Функция ISERROR используется в формулах, которые ссылаются на другую ячейку.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421545"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="4abf9-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4abf9-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4abf9-105">Возвращает значение TRUE, если  _значение cellreference_ имеет какой-либо тип ошибки; в противном случае возвращается false.</span><span class="sxs-lookup"><span data-stu-id="4abf9-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="4abf9-106">Функция ISERROR используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="4abf9-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4abf9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4abf9-107">Syntax</span></span>

<span data-ttu-id="4abf9-108">ISERROR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4abf9-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4abf9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4abf9-109">Parameters</span></span>

|<span data-ttu-id="4abf9-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4abf9-110">**Name**</span></span>|<span data-ttu-id="4abf9-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4abf9-111">**Required/Optional**</span></span>|<span data-ttu-id="4abf9-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4abf9-112">**Data Type**</span></span>|<span data-ttu-id="4abf9-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4abf9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4abf9-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="4abf9-114">_cellreference_</span></span> <br/> |<span data-ttu-id="4abf9-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4abf9-115">Required</span></span>  <br/> |<span data-ttu-id="4abf9-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4abf9-116">**String**</span></span> <br/> |<span data-ttu-id="4abf9-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="4abf9-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="4abf9-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4abf9-118">Example 1</span></span>

|<span data-ttu-id="4abf9-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4abf9-119">**Cell**</span></span>|<span data-ttu-id="4abf9-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4abf9-120">**Formula**</span></span>|<span data-ttu-id="4abf9-121">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="4abf9-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4abf9-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="4abf9-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="4abf9-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="4abf9-123">=NA( )</span></span>  <br/> |<span data-ttu-id="4abf9-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="4abf9-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="4abf9-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="4abf9-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="4abf9-126">=ISERROR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="4abf9-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="4abf9-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="4abf9-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="4abf9-128">Возвращает true, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="4abf9-128">Returns TRUE because the #N/A!</span></span> <span data-ttu-id="4abf9-129">ошибка распознается функцией ISERROR.</span><span class="sxs-lookup"><span data-stu-id="4abf9-129">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="4abf9-130">С помощью ISERR можно найти все типы, кроме #N/A!</span><span class="sxs-lookup"><span data-stu-id="4abf9-130">You can use ISERR to find all types but the #N/A!</span></span> <span data-ttu-id="4abf9-131">error.</span><span class="sxs-lookup"><span data-stu-id="4abf9-131">error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4abf9-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4abf9-132">Example 2</span></span>

|<span data-ttu-id="4abf9-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4abf9-133">**Cell**</span></span>|<span data-ttu-id="4abf9-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4abf9-134">**Formula**</span></span>|<span data-ttu-id="4abf9-135">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="4abf9-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4abf9-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="4abf9-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="4abf9-137">="House"</span><span class="sxs-lookup"><span data-stu-id="4abf9-137">="House"</span></span>  <br/> |<span data-ttu-id="4abf9-138">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="4abf9-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="4abf9-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="4abf9-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="4abf9-140">=ISERROR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="4abf9-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="4abf9-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="4abf9-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="4abf9-142">Возвращает true, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4abf9-142">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="4abf9-143">ошибка распознается функцией ISERROR.</span><span class="sxs-lookup"><span data-stu-id="4abf9-143">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="4abf9-144">Создание выражения на основе #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4abf9-144">To build an expression based on the #VALUE!</span></span> <span data-ttu-id="4abf9-145">ошибка, используйте функцию ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="4abf9-145">error, use the ISERRVALUE function.</span></span>
  

