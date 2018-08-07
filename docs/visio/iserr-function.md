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
description: 'Возвращает значение TRUE, если значение ссылка_на_ячейку имеет любой тип ошибки, кроме # н/д; в противном случае возвращает значение FALSE. Функция ЕОШ используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813983"
---
# <a name="iserr-function"></a><span data-ttu-id="b04d0-104">Функция ISERR</span><span class="sxs-lookup"><span data-stu-id="b04d0-104">ISERR Function</span></span>

<span data-ttu-id="b04d0-105">Возвращает значение TRUE, если значение _ссылка_на_ячейку_ имеет любой тип ошибки, кроме # н/д; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b04d0-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="b04d0-106">Функция ЕОШ используется в формулах, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="b04d0-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b04d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b04d0-107">Syntax</span></span>

<span data-ttu-id="b04d0-108">ЕОШ (** *ссылка_на_ячейку* **)</span><span class="sxs-lookup"><span data-stu-id="b04d0-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b04d0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b04d0-109">Parameters</span></span>

|<span data-ttu-id="b04d0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b04d0-110">**Name**</span></span>|<span data-ttu-id="b04d0-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="b04d0-111">**Required/Optional**</span></span>|<span data-ttu-id="b04d0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b04d0-112">**Data Type**</span></span>|<span data-ttu-id="b04d0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b04d0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b04d0-114">_ссылка_на_ячейку_</span><span class="sxs-lookup"><span data-stu-id="b04d0-114">_cellreference_</span></span> <br/> |<span data-ttu-id="b04d0-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b04d0-115">Required</span></span>  <br/> |<span data-ttu-id="b04d0-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="b04d0-116">**String**</span></span> <br/> |<span data-ttu-id="b04d0-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="b04d0-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="b04d0-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b04d0-118">Example 1</span></span>

|<span data-ttu-id="b04d0-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b04d0-119">**Cell**</span></span>|<span data-ttu-id="b04d0-120">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="b04d0-120">**Formula**</span></span>|<span data-ttu-id="b04d0-121">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="b04d0-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b04d0-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="b04d0-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="b04d0-123">= (НД)</span><span class="sxs-lookup"><span data-stu-id="b04d0-123">=NA( )</span></span>  <br/> |<span data-ttu-id="b04d0-124"># Н/Д!</span><span class="sxs-lookup"><span data-stu-id="b04d0-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="b04d0-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="b04d0-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="b04d0-126">=ISERR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="b04d0-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="b04d0-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="b04d0-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="b04d0-128">Возвращает значение FALSE, так как # н/д!</span><span class="sxs-lookup"><span data-stu-id="b04d0-128">Returns FALSE because the #N/A!</span></span> <span data-ttu-id="b04d0-129">Ошибка не распознается Функция ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="b04d0-129">error is not recognized by the ISERR function.</span></span> <span data-ttu-id="b04d0-130">Чтобы найти все типы ошибок используйте ЕОШИБКА.</span><span class="sxs-lookup"><span data-stu-id="b04d0-130">Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b04d0-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b04d0-131">Example 2</span></span>

|<span data-ttu-id="b04d0-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b04d0-132">**Cell**</span></span>|<span data-ttu-id="b04d0-133">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="b04d0-133">**Formula**</span></span>|<span data-ttu-id="b04d0-134">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="b04d0-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b04d0-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="b04d0-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="b04d0-136">= «Дом»</span><span class="sxs-lookup"><span data-stu-id="b04d0-136">="House"</span></span>  <br/> |<span data-ttu-id="b04d0-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="b04d0-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="b04d0-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="b04d0-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="b04d0-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="b04d0-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="b04d0-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="b04d0-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="b04d0-141">Возвращает значение TRUE, так как #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b04d0-141">Returns TRUE because the #VALUE!</span></span> <span data-ttu-id="b04d0-142">Ошибка распознается Функция ЕОШ.</span><span class="sxs-lookup"><span data-stu-id="b04d0-142">error is recognized by the ISERR function.</span></span>
  

