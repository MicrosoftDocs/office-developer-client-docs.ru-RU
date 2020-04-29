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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432109"
---
# <a name="iserr-function"></a><span data-ttu-id="64fd9-104">Функция ISERR</span><span class="sxs-lookup"><span data-stu-id="64fd9-104">ISERR Function</span></span>

<span data-ttu-id="64fd9-105">Возвращает значение TRUE, если значение _целлреференце_ имеет любой тип ошибки, кроме #N/a; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="64fd9-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="64fd9-106">Функция ЕОШ используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="64fd9-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="64fd9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64fd9-107">Syntax</span></span>

<span data-ttu-id="64fd9-108">ЕОШ (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="64fd9-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="64fd9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64fd9-109">Parameters</span></span>

|<span data-ttu-id="64fd9-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="64fd9-110">**Name**</span></span>|<span data-ttu-id="64fd9-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="64fd9-111">**Required/Optional**</span></span>|<span data-ttu-id="64fd9-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="64fd9-112">**Data Type**</span></span>|<span data-ttu-id="64fd9-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64fd9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="64fd9-114">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="64fd9-114">_cellreference_</span></span> <br/> |<span data-ttu-id="64fd9-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="64fd9-115">Required</span></span>  <br/> |<span data-ttu-id="64fd9-116">**String**</span><span class="sxs-lookup"><span data-stu-id="64fd9-116">**String**</span></span> <br/> |<span data-ttu-id="64fd9-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="64fd9-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="64fd9-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64fd9-118">Example 1</span></span>

|<span data-ttu-id="64fd9-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="64fd9-119">**Cell**</span></span>|<span data-ttu-id="64fd9-120">**Формула**</span><span class="sxs-lookup"><span data-stu-id="64fd9-120">**Formula**</span></span>|<span data-ttu-id="64fd9-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="64fd9-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64fd9-122">". A1"</span><span class="sxs-lookup"><span data-stu-id="64fd9-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="64fd9-123">= НД ()</span><span class="sxs-lookup"><span data-stu-id="64fd9-123">=NA( )</span></span>  <br/> |<span data-ttu-id="64fd9-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="64fd9-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="64fd9-125">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="64fd9-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="64fd9-126">= ЕОШ ("a. a1")</span><span class="sxs-lookup"><span data-stu-id="64fd9-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="64fd9-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="64fd9-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="64fd9-128">Возвращает значение FALSE, так как #N/A!</span><span class="sxs-lookup"><span data-stu-id="64fd9-128">Returns FALSE because the #N/A!</span></span> <span data-ttu-id="64fd9-129">ошибка не распознается функцией ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="64fd9-129">error is not recognized by the ISERR function.</span></span> <span data-ttu-id="64fd9-130">Используйте ЕОШИБКА, чтобы найти все типы ошибок.</span><span class="sxs-lookup"><span data-stu-id="64fd9-130">Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="64fd9-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="64fd9-131">Example 2</span></span>

|<span data-ttu-id="64fd9-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="64fd9-132">**Cell**</span></span>|<span data-ttu-id="64fd9-133">**Формула**</span><span class="sxs-lookup"><span data-stu-id="64fd9-133">**Formula**</span></span>|<span data-ttu-id="64fd9-134">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="64fd9-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64fd9-135">"С начала. x1"</span><span class="sxs-lookup"><span data-stu-id="64fd9-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="64fd9-136">= "Дом"</span><span class="sxs-lookup"><span data-stu-id="64fd9-136">="House"</span></span>  <br/> |<span data-ttu-id="64fd9-137">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="64fd9-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="64fd9-138">". A1"</span><span class="sxs-lookup"><span data-stu-id="64fd9-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="64fd9-139">= ЕОШ ("a. x1")</span><span class="sxs-lookup"><span data-stu-id="64fd9-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="64fd9-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="64fd9-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="64fd9-141">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="64fd9-141">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="64fd9-142">Ошибка распознаваться функцией ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="64fd9-142">error is recognized by the ISERR function.</span></span>
  

