---
title: Функция SETF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Задает формулу ячейки.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425976"
---
# <a name="setf-function"></a><span data-ttu-id="77142-103">Функция SETF</span><span class="sxs-lookup"><span data-stu-id="77142-103">SETF Function</span></span>

<span data-ttu-id="77142-104">Задает формулу ячейки.</span><span class="sxs-lookup"><span data-stu-id="77142-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="77142-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77142-105">Syntax</span></span>

<span data-ttu-id="77142-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span><span class="sxs-lookup"><span data-stu-id="77142-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="77142-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77142-107">Parameters</span></span>

|<span data-ttu-id="77142-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="77142-108">**Name**</span></span>|<span data-ttu-id="77142-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="77142-109">**Required/Optional**</span></span>|<span data-ttu-id="77142-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="77142-110">**Data Type**</span></span>|<span data-ttu-id="77142-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77142-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="77142-112">_cell_</span><span class="sxs-lookup"><span data-stu-id="77142-112">_cell_</span></span> <br/> |<span data-ttu-id="77142-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="77142-113">Required</span></span>  <br/> |<span data-ttu-id="77142-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="77142-114">**String**</span></span> <br/> |<span data-ttu-id="77142-115">Ячейка, формулу которой необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="77142-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="77142-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="77142-116">_formula_</span></span> <br/> |<span data-ttu-id="77142-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="77142-117">Required</span></span>  <br/> |<span data-ttu-id="77142-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="77142-118">**String**</span></span> <br/> |<span data-ttu-id="77142-119">Используемая формула.</span><span class="sxs-lookup"><span data-stu-id="77142-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77142-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="77142-120">Remarks</span></span>

<span data-ttu-id="77142-121">При оценке результат выражения в _формуле_ становится новой формулой в _ячейке._</span><span class="sxs-lookup"><span data-stu-id="77142-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="77142-122">Если _формула_ заключена в кавычках, выражение в кавычках будет записано в _ячейку._</span><span class="sxs-lookup"><span data-stu-id="77142-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="77142-123">Чтобы установить  _для ячейки_ строку, необходимо заключить  _формулу_ в три набора кавычка.</span><span class="sxs-lookup"><span data-stu-id="77142-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="77142-124">Целевая ячейка должна быть указана с помощью ссылки GETREF() или в качестве строки, чтобы избежать цикличности.</span><span class="sxs-lookup"><span data-stu-id="77142-124">The target cell must be specified using a GETREF() reference or as a string to avoid circularity.</span></span> <span data-ttu-id="77142-125">Предпочтительным является использование GETREF, так как Microsoft Visio может настраивать ссылки при перемещении фигуры в другой документ.</span><span class="sxs-lookup"><span data-stu-id="77142-125">Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="77142-126">Если  _ячейка_ не указана с помощью GETREF или в качестве строки, функция возвращает ошибку, и формула ячейки не меняется.</span><span class="sxs-lookup"><span data-stu-id="77142-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="77142-127">Если  _формула_ содержит ошибку синтаксиса, функция возвращает ошибку, а формула в  _ячейке_ не меняется.</span><span class="sxs-lookup"><span data-stu-id="77142-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="77142-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77142-128">Example 1</span></span>

<span data-ttu-id="77142-129">SETF( GETREF(Scratch.A1), 1,5 в \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="77142-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="77142-130">Задает для формулы Scratch.A1 21 дюйма.</span><span class="sxs-lookup"><span data-stu-id="77142-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="77142-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77142-131">Example 2</span></span>

<span data-ttu-id="77142-132">SETF( GETREF(Scratch.A1), "1,5 в \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="77142-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="77142-133">Задает формулу "С нуля".</span><span class="sxs-lookup"><span data-stu-id="77142-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="77142-134">A1 для выражения 1,5 в \* 6+1 ft.</span><span class="sxs-lookup"><span data-stu-id="77142-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="77142-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="77142-135">Example 3</span></span>

<span data-ttu-id="77142-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""</span><span class="sxs-lookup"><span data-stu-id="77142-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="77142-137">Задает формулу Scratch.A1 для строки "Say "ahh"" (Скажите "ahh"), которая оценивается как "ahh".</span><span class="sxs-lookup"><span data-stu-id="77142-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

