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
description: 'Возвращает значение TRUE, если значение целлреференце имеет любой тип ошибки, кроме #N/A; в противном случае возвращает значение FALSE. Функция ЕОШ используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297251"
---
# <a name="iserr-function"></a><span data-ttu-id="99d70-104">Функция ISERR</span><span class="sxs-lookup"><span data-stu-id="99d70-104">ISERR Function</span></span>

<span data-ttu-id="99d70-105">Возвращает значение TRUE, если значение _целлреференце_ имеет любой тип ошибки, кроме #N/a; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="99d70-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="99d70-106">Функция ЕОШ используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="99d70-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="99d70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99d70-107">Syntax</span></span>

<span data-ttu-id="99d70-108">ЕОШ (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="99d70-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="99d70-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99d70-109">Parameters</span></span>

|<span data-ttu-id="99d70-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="99d70-110">**Name**</span></span>|<span data-ttu-id="99d70-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="99d70-111">**Required/Optional**</span></span>|<span data-ttu-id="99d70-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="99d70-112">**Data Type**</span></span>|<span data-ttu-id="99d70-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="99d70-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="99d70-114">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="99d70-114">_cellreference_</span></span> <br/> |<span data-ttu-id="99d70-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="99d70-115">Required</span></span>  <br/> |<span data-ttu-id="99d70-116">**String**</span><span class="sxs-lookup"><span data-stu-id="99d70-116">**String**</span></span> <br/> |<span data-ttu-id="99d70-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="99d70-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="99d70-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99d70-118">Example 1</span></span>

|<span data-ttu-id="99d70-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="99d70-119">**Cell**</span></span>|<span data-ttu-id="99d70-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="99d70-120">**Formula**</span></span>|<span data-ttu-id="99d70-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="99d70-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99d70-122">". A1"</span><span class="sxs-lookup"><span data-stu-id="99d70-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="99d70-123">= НД ()</span><span class="sxs-lookup"><span data-stu-id="99d70-123">=NA( )</span></span>  <br/> |<span data-ttu-id="99d70-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="99d70-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="99d70-125">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="99d70-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="99d70-126">= ЕОШ ("a. a1")</span><span class="sxs-lookup"><span data-stu-id="99d70-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="99d70-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="99d70-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="99d70-128">Возвращает значение FALSE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="99d70-128">Returns FALSE because the #N/A!</span></span> <span data-ttu-id="99d70-129">ошибка не распознается функцией ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="99d70-129">error is not recognized by the ISERR function.</span></span> <span data-ttu-id="99d70-130">Используйте ЕОШИБКА, чтобы найти все типы ошибок.</span><span class="sxs-lookup"><span data-stu-id="99d70-130">Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="99d70-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99d70-131">Example 2</span></span>

|<span data-ttu-id="99d70-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="99d70-132">**Cell**</span></span>|<span data-ttu-id="99d70-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="99d70-133">**Formula**</span></span>|<span data-ttu-id="99d70-134">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="99d70-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99d70-135">"С начала. x1"</span><span class="sxs-lookup"><span data-stu-id="99d70-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="99d70-136">= "Дом"</span><span class="sxs-lookup"><span data-stu-id="99d70-136">="House"</span></span>  <br/> |<span data-ttu-id="99d70-137">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="99d70-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="99d70-138">". A1"</span><span class="sxs-lookup"><span data-stu-id="99d70-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="99d70-139">= ЕОШ ("a. x1")</span><span class="sxs-lookup"><span data-stu-id="99d70-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="99d70-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="99d70-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="99d70-141">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="99d70-141">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="99d70-142">Ошибка распознаваться функцией ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="99d70-142">error is recognized by the ISERR function.</span></span>
  

