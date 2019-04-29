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
# <a name="setf-function"></a><span data-ttu-id="b810c-103">Функция SETF</span><span class="sxs-lookup"><span data-stu-id="b810c-103">SETF Function</span></span>

<span data-ttu-id="b810c-104">Задает формулу ячейки.</span><span class="sxs-lookup"><span data-stu-id="b810c-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b810c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b810c-105">Syntax</span></span>

<span data-ttu-id="b810c-106">SETF (GETREF (\* \* *ячейка* \* \*), \* \* *Формула* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b810c-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b810c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b810c-107">Parameters</span></span>

|<span data-ttu-id="b810c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b810c-108">**Name**</span></span>|<span data-ttu-id="b810c-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b810c-109">**Required/Optional**</span></span>|<span data-ttu-id="b810c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b810c-110">**Data Type**</span></span>|<span data-ttu-id="b810c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b810c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b810c-112">_элемент_</span><span class="sxs-lookup"><span data-stu-id="b810c-112">_cell_</span></span> <br/> |<span data-ttu-id="b810c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b810c-113">Required</span></span>  <br/> |<span data-ttu-id="b810c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b810c-114">**String**</span></span> <br/> |<span data-ttu-id="b810c-115">Ячейка, для которой задается формула.</span><span class="sxs-lookup"><span data-stu-id="b810c-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="b810c-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="b810c-116">_formula_</span></span> <br/> |<span data-ttu-id="b810c-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b810c-117">Required</span></span>  <br/> |<span data-ttu-id="b810c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b810c-118">**String**</span></span> <br/> |<span data-ttu-id="b810c-119">Используемая формула.</span><span class="sxs-lookup"><span data-stu-id="b810c-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b810c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b810c-120">Remarks</span></span>

<span data-ttu-id="b810c-121">При оценке результат выражения в формуле становится новой __ формулой в ячейке. __</span><span class="sxs-lookup"><span data-stu-id="b810c-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="b810c-122">Если _Формула_ заключена в кавычки, выражение с кавычками записывается в _ячейку_.</span><span class="sxs-lookup"><span data-stu-id="b810c-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="b810c-123">Чтобы присвоить _ячейке_ строку, заключите _формулу_ в три набора кавычек.</span><span class="sxs-lookup"><span data-stu-id="b810c-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="b810c-124">Целевую ячейку необходимо указать с помощью ссылки на GETREF () или в виде строки, чтобы избежать цикличности.</span><span class="sxs-lookup"><span data-stu-id="b810c-124">The target cell must be specified using a GETREF() reference or as a string to avoid circularity.</span></span> <span data-ttu-id="b810c-125">Рекомендуется использовать GETREF, так как Microsoft Visio может скорректировать ссылки при перемещении фигуры в другой документ.</span><span class="sxs-lookup"><span data-stu-id="b810c-125">Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="b810c-126">Если _ячейка_ не указана с помощью GETREF или строки, функция возвращает ошибку, а формула ячейки не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b810c-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="b810c-127">Если _Формула_ содержит синтаксическую ошибку, функция возвращает ошибку, а формула в ячейке не изменяется __ .</span><span class="sxs-lookup"><span data-stu-id="b810c-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b810c-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b810c-128">Example 1</span></span>

<span data-ttu-id="b810c-129">SETF (GETREF ("с нуля. a1), \* 1,5 в 6 + 1 ФТ)</span><span class="sxs-lookup"><span data-stu-id="b810c-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="b810c-130">Задает формулу "с нуля" до 21 дюймов.</span><span class="sxs-lookup"><span data-stu-id="b810c-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b810c-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b810c-131">Example 2</span></span>

<span data-ttu-id="b810c-132">SETF (GETREF ("с нуля. a1"), \* "1,5" в 6 + 1 ФТ)</span><span class="sxs-lookup"><span data-stu-id="b810c-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="b810c-133">Задает формулу "с нуля".</span><span class="sxs-lookup"><span data-stu-id="b810c-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="b810c-134">A1 на выражение 1,5 в\*6 + 1 ФТ.</span><span class="sxs-lookup"><span data-stu-id="b810c-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b810c-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b810c-135">Example 3</span></span>

<span data-ttu-id="b810c-136">SETF (GETREF ("с нуля. a1"), "" "" "" "" "АХХ" "" "" ")</span><span class="sxs-lookup"><span data-stu-id="b810c-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="b810c-137">Задает формулу "" с начала. a1 "на строку" Скажите "" АХХ "" "(" ""), которая оценивается как "АХХ".</span><span class="sxs-lookup"><span data-stu-id="b810c-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

