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
description: 'Возвращает значение TRUE, если значение cellreference имеет какой-либо тип ошибки, кроме #N/A; в противном случае возвращается false. Функция ISERR используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432109"
---
# <a name="iserr-function"></a><span data-ttu-id="4f4ba-104">Функция ISERR</span><span class="sxs-lookup"><span data-stu-id="4f4ba-104">ISERR Function</span></span>

<span data-ttu-id="4f4ba-105">Возвращает значение TRUE, если значение  _cellreference_ имеет какой-либо тип ошибки, кроме #N/A; в противном случае возвращается false.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="4f4ba-106">Функция ISERR используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4f4ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f4ba-107">Syntax</span></span>

<span data-ttu-id="4f4ba-108">ISERR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4f4ba-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4f4ba-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f4ba-109">Parameters</span></span>

|<span data-ttu-id="4f4ba-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-110">**Name**</span></span>|<span data-ttu-id="4f4ba-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-111">**Required/Optional**</span></span>|<span data-ttu-id="4f4ba-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-112">**Data Type**</span></span>|<span data-ttu-id="4f4ba-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4f4ba-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="4f4ba-114">_cellreference_</span></span> <br/> |<span data-ttu-id="4f4ba-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4f4ba-115">Required</span></span>  <br/> |<span data-ttu-id="4f4ba-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-116">**String**</span></span> <br/> |<span data-ttu-id="4f4ba-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="4f4ba-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f4ba-118">Example 1</span></span>

|<span data-ttu-id="4f4ba-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-119">**Cell**</span></span>|<span data-ttu-id="4f4ba-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-120">**Formula**</span></span>|<span data-ttu-id="4f4ba-121">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f4ba-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="4f4ba-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="4f4ba-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="4f4ba-123">=NA( )</span></span>  <br/> |<span data-ttu-id="4f4ba-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="4f4ba-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="4f4ba-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="4f4ba-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="4f4ba-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="4f4ba-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="4f4ba-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f4ba-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="4f4ba-128">Возвращает false, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="4f4ba-128">Returns FALSE because the #N/A!</span></span> <span data-ttu-id="4f4ba-129">ошибка не распознается функцией ISERR.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-129">error is not recognized by the ISERR function.</span></span> <span data-ttu-id="4f4ba-130">Используйте ISERROR для поиска всех типов ошибок.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-130">Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4f4ba-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4f4ba-131">Example 2</span></span>

|<span data-ttu-id="4f4ba-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-132">**Cell**</span></span>|<span data-ttu-id="4f4ba-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-133">**Formula**</span></span>|<span data-ttu-id="4f4ba-134">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f4ba-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="4f4ba-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="4f4ba-136">="House"</span><span class="sxs-lookup"><span data-stu-id="4f4ba-136">="House"</span></span>  <br/> |<span data-ttu-id="4f4ba-137">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="4f4ba-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="4f4ba-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="4f4ba-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="4f4ba-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="4f4ba-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="4f4ba-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f4ba-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="4f4ba-141">Возвращает true, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4f4ba-141">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="4f4ba-142">ошибка распознается функцией ISERR.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-142">error is recognized by the ISERR function.</span></span>
  

