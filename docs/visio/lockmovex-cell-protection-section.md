---
title: LockMoveX Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Блокирует горизонтальное положение фигуры, поэтому ее невозможно по горизонтали.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435861"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="e3beb-103">LockMoveX Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="e3beb-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="e3beb-104">Блокирует горизонтальное положение фигуры, поэтому ее невозможно по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="e3beb-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="e3beb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e3beb-105">**Value**</span></span>|<span data-ttu-id="e3beb-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3beb-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e3beb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e3beb-107">TRUE</span></span>  <br/> | <span data-ttu-id="e3beb-108">Горизонтальное положение заблокировано.</span><span class="sxs-lookup"><span data-stu-id="e3beb-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="e3beb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3beb-109">FALSE</span></span>  <br/> | <span data-ttu-id="e3beb-110">Горизонтальное положение не заблокировано.</span><span class="sxs-lookup"><span data-stu-id="e3beb-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3beb-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3beb-111">Remarks</span></span>

<span data-ttu-id="e3beb-112">Чтобы получить ссылку на ячейку LockMoveX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e3beb-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3beb-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3beb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e3beb-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="e3beb-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="e3beb-115">Чтобы получить ссылку на ячейку LockMoveX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e3beb-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3beb-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3beb-116">Section index:</span></span>  <br/> |<span data-ttu-id="e3beb-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3beb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e3beb-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3beb-118">Row index:</span></span>  <br/> |<span data-ttu-id="e3beb-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e3beb-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e3beb-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3beb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e3beb-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="e3beb-121">**visLockMoveX**</span></span> <br/> |
   

