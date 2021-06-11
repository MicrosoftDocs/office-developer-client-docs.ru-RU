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
description: Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — это тип ошибки; в противном случае возвращает FALSE. Функция ISERROR используется в формулах, которые относятся к другой ячейке.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421545"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="fc38e-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fc38e-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fc38e-105">Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — это тип ошибки; в противном случае возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="fc38e-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="fc38e-106">Функция ISERROR используется в формулах, которые относятся к другой ячейке.</span><span class="sxs-lookup"><span data-stu-id="fc38e-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fc38e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc38e-107">Syntax</span></span>

<span data-ttu-id="fc38e-108">ISERROR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fc38e-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fc38e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc38e-109">Parameters</span></span>

|<span data-ttu-id="fc38e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fc38e-110">**Name**</span></span>|<span data-ttu-id="fc38e-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fc38e-111">**Required/Optional**</span></span>|<span data-ttu-id="fc38e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fc38e-112">**Data Type**</span></span>|<span data-ttu-id="fc38e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc38e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fc38e-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="fc38e-114">_cellreference_</span></span> <br/> |<span data-ttu-id="fc38e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc38e-115">Required</span></span>  <br/> |<span data-ttu-id="fc38e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="fc38e-116">**String**</span></span> <br/> |<span data-ttu-id="fc38e-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="fc38e-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="fc38e-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc38e-118">Example 1</span></span>

|<span data-ttu-id="fc38e-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fc38e-119">**Cell**</span></span>|<span data-ttu-id="fc38e-120">**Формула**</span><span class="sxs-lookup"><span data-stu-id="fc38e-120">**Formula**</span></span>|<span data-ttu-id="fc38e-121">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="fc38e-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc38e-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="fc38e-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="fc38e-123">=NA()</span><span class="sxs-lookup"><span data-stu-id="fc38e-123">=NA( )</span></span>  <br/> |<span data-ttu-id="fc38e-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="fc38e-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="fc38e-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="fc38e-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fc38e-126">=ISERROR (Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="fc38e-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="fc38e-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="fc38e-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="fc38e-128">Возвращает TRUE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="fc38e-128">Returns TRUE because the #N/A!</span></span> <span data-ttu-id="fc38e-129">ошибка распознается функцией ISERROR.</span><span class="sxs-lookup"><span data-stu-id="fc38e-129">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="fc38e-130">Вы можете использовать ISERR для поиска всех типов, кроме #N/A!</span><span class="sxs-lookup"><span data-stu-id="fc38e-130">You can use ISERR to find all types but the #N/A!</span></span> <span data-ttu-id="fc38e-131">ошибка.</span><span class="sxs-lookup"><span data-stu-id="fc38e-131">error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fc38e-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fc38e-132">Example 2</span></span>

|<span data-ttu-id="fc38e-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fc38e-133">**Cell**</span></span>|<span data-ttu-id="fc38e-134">**Формула**</span><span class="sxs-lookup"><span data-stu-id="fc38e-134">**Formula**</span></span>|<span data-ttu-id="fc38e-135">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="fc38e-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc38e-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="fc38e-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="fc38e-137">="Дом"</span><span class="sxs-lookup"><span data-stu-id="fc38e-137">="House"</span></span>  <br/> |<span data-ttu-id="fc38e-138">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="fc38e-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="fc38e-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="fc38e-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fc38e-140">=ISERROR (Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="fc38e-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="fc38e-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="fc38e-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="fc38e-142">Возвращает TRUE, потому что #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fc38e-142">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="fc38e-143">ошибка распознается функцией ISERROR.</span><span class="sxs-lookup"><span data-stu-id="fc38e-143">error is recognized by the ISERROR function.</span></span> <span data-ttu-id="fc38e-144">Создание выражения на основе #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fc38e-144">To build an expression based on the #VALUE!</span></span> <span data-ttu-id="fc38e-145">ошибка, используйте функцию ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="fc38e-145">error, use the ISERRVALUE function.</span></span>
  

