---
title: Функция ISERRNA
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — тип #N/A! (недоступны); в противном случае возвращает FALSE. Функция ISERRNA используется в формулах, которые относятся к другой ячейке.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432116"
---
# <a name="iserrna-function"></a><span data-ttu-id="d5714-105">Функция ISERRNA</span><span class="sxs-lookup"><span data-stu-id="d5714-105">ISERRNA Function</span></span>

<span data-ttu-id="d5714-106">Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — тип #N/A!</span><span class="sxs-lookup"><span data-stu-id="d5714-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="d5714-107">(недоступны); в противном случае возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="d5714-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="d5714-108">Функция ISERRNA используется в формулах, которые относятся к другой ячейке.</span><span class="sxs-lookup"><span data-stu-id="d5714-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d5714-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5714-109">Syntax</span></span>

<span data-ttu-id="d5714-110">ISERRNA(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d5714-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d5714-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5714-111">Parameters</span></span>

|<span data-ttu-id="d5714-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d5714-112">**Name**</span></span>|<span data-ttu-id="d5714-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d5714-113">**Required/Optional**</span></span>|<span data-ttu-id="d5714-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d5714-114">**Data Type**</span></span>|<span data-ttu-id="d5714-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5714-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d5714-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="d5714-116">_cellreference_</span></span> <br/> |<span data-ttu-id="d5714-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d5714-117">Required</span></span>  <br/> |<span data-ttu-id="d5714-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d5714-118">**String**</span></span> <br/> |<span data-ttu-id="d5714-119">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="d5714-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d5714-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5714-120">Example 1</span></span>

|<span data-ttu-id="d5714-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d5714-121">**Cell**</span></span>|<span data-ttu-id="d5714-122">**Формула**</span><span class="sxs-lookup"><span data-stu-id="d5714-122">**Formula**</span></span>|<span data-ttu-id="d5714-123">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="d5714-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5714-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="d5714-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="d5714-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="d5714-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="d5714-126">"8"</span><span class="sxs-lookup"><span data-stu-id="d5714-126">"8"</span></span>  <br/> |
|<span data-ttu-id="d5714-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="d5714-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d5714-128">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="d5714-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="d5714-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="d5714-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="d5714-130">Возвращает FALSE, так как возвращенные значения доступны.</span><span class="sxs-lookup"><span data-stu-id="d5714-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d5714-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d5714-131">Example 2</span></span>

|<span data-ttu-id="d5714-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d5714-132">**Cell**</span></span>|<span data-ttu-id="d5714-133">**Формула**</span><span class="sxs-lookup"><span data-stu-id="d5714-133">**Formula**</span></span>|<span data-ttu-id="d5714-134">**Возвращено значение**</span><span class="sxs-lookup"><span data-stu-id="d5714-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5714-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="d5714-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="d5714-136">=NA()</span><span class="sxs-lookup"><span data-stu-id="d5714-136">=NA( )</span></span>  <br/> |<span data-ttu-id="d5714-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="d5714-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="d5714-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="d5714-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d5714-139">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="d5714-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="d5714-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="d5714-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="d5714-141">Возвращает ЗНАЧЕНИЕ TRUE, так как возвращено значение типа #N/A!</span><span class="sxs-lookup"><span data-stu-id="d5714-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

