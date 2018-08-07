---
title: Ячейка SketchAmount (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Определяет объем искажений эффект эскиза, как целое число от 0 до 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814879"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="93410-103">Ячейка SketchAmount (раздел "Дополнительные свойства эффекта")</span><span class="sxs-lookup"><span data-stu-id="93410-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="93410-104">Определяет объем искажений эффект эскиза, как целое число от 0 до 25.</span><span class="sxs-lookup"><span data-stu-id="93410-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="93410-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="93410-105">**Value**</span></span>|<span data-ttu-id="93410-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93410-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93410-107">0</span><span class="sxs-lookup"><span data-stu-id="93410-107">0</span></span>  <br/> |<span data-ttu-id="93410-108">Фигура не действует эскиза применяется к нему.</span><span class="sxs-lookup"><span data-stu-id="93410-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="93410-109">1-25</span><span class="sxs-lookup"><span data-stu-id="93410-109">1-25</span></span>  <br/> |<span data-ttu-id="93410-110">Фигура имеет искажений эскиза применяется к нему, где значение 1: большинство искажений и 25 – меньше всего.</span><span class="sxs-lookup"><span data-stu-id="93410-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93410-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="93410-111">Remarks</span></span>

<span data-ttu-id="93410-112">Для получения ссылки на ячейки **SketchAmount** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="93410-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93410-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="93410-113">Cell name:</span></span>  <br/> | <span data-ttu-id="93410-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="93410-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="93410-115">Для получения ссылки на ячейки **SketchAmount** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="93410-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93410-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93410-116">Section index:</span></span>  <br/> |<span data-ttu-id="93410-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93410-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="93410-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93410-118">Row index:</span></span>  <br/> |<span data-ttu-id="93410-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="93410-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="93410-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93410-120">Cell index:</span></span>  <br/> |<span data-ttu-id="93410-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="93410-121">**visSketchAmount**</span></span> <br/> |
   

