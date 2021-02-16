---
title: LockCalcWH Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при редактировании вершины или при смене типа строки в разделе "Геометрия".
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423043"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="eabd3-103">LockCalcWH Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="eabd3-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="eabd3-104">Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при редактировании вершины или при смене типа строки в разделе "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="eabd3-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="eabd3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="eabd3-105">**Value**</span></span>|<span data-ttu-id="eabd3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eabd3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eabd3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eabd3-107">TRUE</span></span>  <br/> | <span data-ttu-id="eabd3-108">Ширина и высота не могут быть пересчитаны.</span><span class="sxs-lookup"><span data-stu-id="eabd3-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="eabd3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eabd3-109">FALSE</span></span>  <br/> | <span data-ttu-id="eabd3-110">Можно пересчитать ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="eabd3-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eabd3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="eabd3-111">Remarks</span></span>

<span data-ttu-id="eabd3-112">Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="eabd3-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eabd3-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eabd3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="eabd3-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="eabd3-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="eabd3-115">Чтобы получить ссылку на ячейку LockCalcWH по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eabd3-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eabd3-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eabd3-116">Section index:</span></span>  <br/> |<span data-ttu-id="eabd3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eabd3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eabd3-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eabd3-118">Row index:</span></span>  <br/> |<span data-ttu-id="eabd3-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="eabd3-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="eabd3-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eabd3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="eabd3-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="eabd3-121">**visLockCalcWH**</span></span> <br/> |
   

