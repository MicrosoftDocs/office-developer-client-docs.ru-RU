---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет количество искажений для эффекты эскиза в виде целого числа от 0 до 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404423"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="bc184-103">SketchAmount Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="bc184-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="bc184-104">Определяет количество искажений для эффекты эскиза в виде целого числа от 0 до 25.</span><span class="sxs-lookup"><span data-stu-id="bc184-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="bc184-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bc184-105">**Value**</span></span>|<span data-ttu-id="bc184-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bc184-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc184-107">нуль</span><span class="sxs-lookup"><span data-stu-id="bc184-107">0</span></span>  <br/> |<span data-ttu-id="bc184-108">К фигуре не применены эффекты эскиза.</span><span class="sxs-lookup"><span data-stu-id="bc184-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="bc184-109">1-25</span><span class="sxs-lookup"><span data-stu-id="bc184-109">1-25</span></span>  <br/> |<span data-ttu-id="bc184-110">К фигуре применено искажение эскизов, где значение 1 является самым подмножеством искажений, а 25 — наименьшей.</span><span class="sxs-lookup"><span data-stu-id="bc184-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc184-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc184-111">Remarks</span></span>

<span data-ttu-id="bc184-112">Чтобы получить ссылку на ячейку **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="bc184-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc184-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bc184-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bc184-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="bc184-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="bc184-115">Чтобы получить ссылку на ячейку **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bc184-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc184-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bc184-116">Section index:</span></span>  <br/> |<span data-ttu-id="bc184-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bc184-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bc184-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bc184-118">Row index:</span></span>  <br/> |<span data-ttu-id="bc184-119">**висровосереффектпропертиес**</span><span class="sxs-lookup"><span data-stu-id="bc184-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="bc184-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bc184-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bc184-121">**висскетчамаунт**</span><span class="sxs-lookup"><span data-stu-id="bc184-121">**visSketchAmount**</span></span> <br/> |
   

