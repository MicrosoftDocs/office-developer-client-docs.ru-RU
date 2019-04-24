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
description: Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при изменении вершины или при изменении типа строки в разделе Geometry.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359635"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="3a22c-103">LockCalcWH Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="3a22c-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="3a22c-104">Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при изменении вершины или при изменении типа строки в разделе Geometry.</span><span class="sxs-lookup"><span data-stu-id="3a22c-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="3a22c-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="3a22c-105">**Value**</span></span>|<span data-ttu-id="3a22c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a22c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3a22c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a22c-107">TRUE</span></span>  <br/> | <span data-ttu-id="3a22c-108">Невозможно пересчитать ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="3a22c-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="3a22c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a22c-109">FALSE</span></span>  <br/> | <span data-ttu-id="3a22c-110">Можно пересчитать ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="3a22c-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a22c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a22c-111">Remarks</span></span>

<span data-ttu-id="3a22c-112">Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3a22c-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a22c-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3a22c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3a22c-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="3a22c-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="3a22c-115">Чтобы получить ссылку на ячейку LockCalcWH по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3a22c-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a22c-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3a22c-116">Section index:</span></span>  <br/> |<span data-ttu-id="3a22c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a22c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3a22c-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3a22c-118">Row index:</span></span>  <br/> |<span data-ttu-id="3a22c-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="3a22c-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3a22c-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3a22c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3a22c-121">**Вислокккалквх**</span><span class="sxs-lookup"><span data-stu-id="3a22c-121">**visLockCalcWH**</span></span> <br/> |
   

