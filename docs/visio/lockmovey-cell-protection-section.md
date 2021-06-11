---
title: LockMoveY Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Блокирует вертикальное положение фигуры, чтобы она не перемещалась по вертикали.
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434048"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="c0b8d-103">LockMoveY Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="c0b8d-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="c0b8d-104">Блокирует вертикальное положение фигуры, чтобы она не перемещалась по вертикали.</span><span class="sxs-lookup"><span data-stu-id="c0b8d-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="c0b8d-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c0b8d-105">**Value**</span></span>|<span data-ttu-id="c0b8d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0b8d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c0b8d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0b8d-107">TRUE</span></span>  <br/> | <span data-ttu-id="c0b8d-108">Вертикальное положение заблокировано.</span><span class="sxs-lookup"><span data-stu-id="c0b8d-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="c0b8d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0b8d-109">FALSE</span></span>  <br/> | <span data-ttu-id="c0b8d-110">Вертикальное положение не заблокировано.</span><span class="sxs-lookup"><span data-stu-id="c0b8d-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0b8d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0b8d-111">Remarks</span></span>

<span data-ttu-id="c0b8d-112">Чтобы получить ссылку на ячейку LockMoveY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0b8d-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c0b8d-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="c0b8d-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="c0b8d-115">Чтобы получить ссылку на ячейку LockMoveY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0b8d-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-116">Section index:</span></span>  <br/> |<span data-ttu-id="c0b8d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0b8d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0b8d-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-118">Row index:</span></span>  <br/> |<span data-ttu-id="c0b8d-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c0b8d-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c0b8d-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0b8d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c0b8d-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="c0b8d-121">**visLockMoveY**</span></span> <br/> |
   

