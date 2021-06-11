---
title: Функция ISERR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — это тип ошибок, за исключением #N/A; в противном случае возвращает FALSE. Функция ISERR используется в формулах, которые относятся к другой ячейке.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432109"
---
# <a name="iserr-function"></a><span data-ttu-id="3b159-104">Функция ISERR</span><span class="sxs-lookup"><span data-stu-id="3b159-104">ISERR Function</span></span>

<span data-ttu-id="3b159-105">Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — это тип ошибок, за исключением #N/A; в противном случае возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="3b159-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="3b159-106">Функция ISERR используется в формулах, которые относятся к другой ячейке.</span><span class="sxs-lookup"><span data-stu-id="3b159-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b159-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b159-107">Syntax</span></span>

<span data-ttu-id="3b159-108">ISERR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3b159-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3b159-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b159-109">Parameters</span></span>

|<span data-ttu-id="3b159-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3b159-110">**Name**</span></span>|<span data-ttu-id="3b159-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3b159-111">**Required/Optional**</span></span>|<span data-ttu-id="3b159-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3b159-112">**Data Type**</span></span>|<span data-ttu-id="3b159-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b159-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3b159-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="3b159-114">_cellreference_</span></span> <br/> |<span data-ttu-id="3b159-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3b159-115">Required</span></span>  <br/> |<span data-ttu-id="3b159-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3b159-116">**String**</span></span> <br/> |<span data-ttu-id="3b159-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="3b159-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3b159-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b159-118">Example 1</span></span>

|<span data-ttu-id="3b159-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b159-119">**Cell**</span></span>|<span data-ttu-id="3b159-120">**Формула**</span><span class="sxs-lookup"><span data-stu-id="3b159-120">**Formula**</span></span>|<span data-ttu-id="3b159-121">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="3b159-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b159-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="3b159-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3b159-123">=NA()</span><span class="sxs-lookup"><span data-stu-id="3b159-123">=NA( )</span></span>  <br/> |<span data-ttu-id="3b159-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="3b159-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="3b159-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="3b159-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="3b159-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="3b159-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="3b159-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b159-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="3b159-128">Возвращает FALSE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="3b159-128">Returns FALSE because the #N/A!</span></span> <span data-ttu-id="3b159-129">ошибка не распознается функцией ISERR.</span><span class="sxs-lookup"><span data-stu-id="3b159-129">error is not recognized by the ISERR function.</span></span> <span data-ttu-id="3b159-130">Используйте ISERROR, чтобы найти все типы ошибок.</span><span class="sxs-lookup"><span data-stu-id="3b159-130">Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3b159-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3b159-131">Example 2</span></span>

|<span data-ttu-id="3b159-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b159-132">**Cell**</span></span>|<span data-ttu-id="3b159-133">**Формула**</span><span class="sxs-lookup"><span data-stu-id="3b159-133">**Formula**</span></span>|<span data-ttu-id="3b159-134">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="3b159-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b159-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="3b159-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="3b159-136">="Дом"</span><span class="sxs-lookup"><span data-stu-id="3b159-136">="House"</span></span>  <br/> |<span data-ttu-id="3b159-137">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="3b159-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="3b159-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="3b159-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3b159-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="3b159-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="3b159-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b159-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="3b159-141">Возвращает TRUE, потому что #VALUE!</span><span class="sxs-lookup"><span data-stu-id="3b159-141">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="3b159-142">ошибка распознается функцией ISERR.</span><span class="sxs-lookup"><span data-stu-id="3b159-142">error is recognized by the ISERR function.</span></span>
  

