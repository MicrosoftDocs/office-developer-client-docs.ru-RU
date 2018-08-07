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
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814750"
---
# <a name="setf-function"></a><span data-ttu-id="519d1-103">Функция SETF</span><span class="sxs-lookup"><span data-stu-id="519d1-103">SETF Function</span></span>

<span data-ttu-id="519d1-104">Задает формулу ячейки.</span><span class="sxs-lookup"><span data-stu-id="519d1-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="519d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="519d1-105">Syntax</span></span>

<span data-ttu-id="519d1-106">SETF (GETREF (** *ячейки* **), ** *Формула* **)</span><span class="sxs-lookup"><span data-stu-id="519d1-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="519d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="519d1-107">Parameters</span></span>

|<span data-ttu-id="519d1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="519d1-108">**Name**</span></span>|<span data-ttu-id="519d1-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="519d1-109">**Required/Optional**</span></span>|<span data-ttu-id="519d1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="519d1-110">**Data Type**</span></span>|<span data-ttu-id="519d1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="519d1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="519d1-112">_ячейки_</span><span class="sxs-lookup"><span data-stu-id="519d1-112">_cell_</span></span> <br/> |<span data-ttu-id="519d1-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="519d1-113">Required</span></span>  <br/> |<span data-ttu-id="519d1-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="519d1-114">**String**</span></span> <br/> |<span data-ttu-id="519d1-115">Ячейки, формулы, чтобы задать.</span><span class="sxs-lookup"><span data-stu-id="519d1-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="519d1-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="519d1-116">_formula_</span></span> <br/> |<span data-ttu-id="519d1-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="519d1-117">Required</span></span>  <br/> |<span data-ttu-id="519d1-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="519d1-118">**String**</span></span> <br/> |<span data-ttu-id="519d1-119">Формула для.</span><span class="sxs-lookup"><span data-stu-id="519d1-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="519d1-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="519d1-120">Remarks</span></span>

<span data-ttu-id="519d1-121">При выполнении функции, в результате выражение в _формуле_ становится новые формулы в _ячейке_.</span><span class="sxs-lookup"><span data-stu-id="519d1-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="519d1-122">Если _формуле_ заключен в кавычки, кавычках выражение записывается в _ячейку_.</span><span class="sxs-lookup"><span data-stu-id="519d1-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="519d1-123">Чтобы задать _ячейки_ в строку, заключите _формулы_ в трех наборов кавычки.</span><span class="sxs-lookup"><span data-stu-id="519d1-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="519d1-124">Целевой ячейки должен быть указан с помощью ссылки на GETREF() или в виде строки во избежание циклические ссылки.</span><span class="sxs-lookup"><span data-stu-id="519d1-124">The target cell must be specified using a GETREF() reference or as a string to avoid circularity.</span></span> <span data-ttu-id="519d1-125">С помощью GETREF является более предпочтительным, так как Microsoft Visio можно настроить ссылки, при перемещении фигуры в другой документ.</span><span class="sxs-lookup"><span data-stu-id="519d1-125">Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="519d1-126">Если _ячейки_ не указан с помощью GETREF или в виде строки, функция возвращает ошибку и не ячейка изменяется.</span><span class="sxs-lookup"><span data-stu-id="519d1-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="519d1-127">Если _Формула_ содержит синтаксическая ошибка, функция возвращает ошибку, и формулы в _ячейке_ не изменяется.</span><span class="sxs-lookup"><span data-stu-id="519d1-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="519d1-128">Пример 1</span><span class="sxs-lookup"><span data-stu-id="519d1-128">Example 1</span></span>

<span data-ttu-id="519d1-129">SETF (GETREF(Scratch.A1), 1,5 в \* 6 + 1 футов)</span><span class="sxs-lookup"><span data-stu-id="519d1-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="519d1-130">Задает формулу Scratch.A1 21 см.</span><span class="sxs-lookup"><span data-stu-id="519d1-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="519d1-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="519d1-131">Example 2</span></span>

<span data-ttu-id="519d1-132">SETF (GETREF(Scratch.A1), «1,5 в \* 6 + 1 ft»)</span><span class="sxs-lookup"><span data-stu-id="519d1-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="519d1-133">Задает формулу нуля.</span><span class="sxs-lookup"><span data-stu-id="519d1-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="519d1-134">A1 на него 1,5 в\*ft 6 + 1.</span><span class="sxs-lookup"><span data-stu-id="519d1-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="519d1-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="519d1-135">Example 3</span></span>

<span data-ttu-id="519d1-136">SETF (GETREF(Scratch.A1), «"«Сказать «««ahh»»»)</span><span class="sxs-lookup"><span data-stu-id="519d1-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="519d1-137">Задает формулу Scratch.A1 в строку «Сказать ««ahh»»» имеющее сказать «ahh».</span><span class="sxs-lookup"><span data-stu-id="519d1-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

