---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет искажение эффекта наброска в качестве количества от 0 до 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404423"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="4bae9-103">SketchAmount Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4bae9-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4bae9-104">Определяет искажение эффекта наброска в качестве количества от 0 до 25.</span><span class="sxs-lookup"><span data-stu-id="4bae9-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="4bae9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4bae9-105">**Value**</span></span>|<span data-ttu-id="4bae9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4bae9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bae9-107">0</span><span class="sxs-lookup"><span data-stu-id="4bae9-107">0</span></span>  <br/> |<span data-ttu-id="4bae9-108">К фигуре не применяется эффект наброска.</span><span class="sxs-lookup"><span data-stu-id="4bae9-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="4bae9-109">1-25</span><span class="sxs-lookup"><span data-stu-id="4bae9-109">1-25</span></span>  <br/> |<span data-ttu-id="4bae9-110">К фигуре применено искажение эскиза, где значение 1 является самым искажением, а 25 — наименьшим.</span><span class="sxs-lookup"><span data-stu-id="4bae9-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bae9-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bae9-111">Remarks</span></span>

<span data-ttu-id="4bae9-112">Чтобы получить ссылку на ячейку **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4bae9-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4bae9-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4bae9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4bae9-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="4bae9-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="4bae9-115">Чтобы получить ссылку на ячейку **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4bae9-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4bae9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4bae9-116">Section index:</span></span>  <br/> |<span data-ttu-id="4bae9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4bae9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4bae9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4bae9-118">Row index:</span></span>  <br/> |<span data-ttu-id="4bae9-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4bae9-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4bae9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4bae9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4bae9-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="4bae9-121">**visSketchAmount**</span></span> <br/> |
   

