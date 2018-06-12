---
title: Ячейка LockMoveX (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Блокирует горизонтальную позицию фигуры, чтобы он не перемещаться по горизонтали.
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814154"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="d37bc-103">Ячейка LockMoveX (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="d37bc-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="d37bc-104">Блокирует горизонтальную позицию фигуры, чтобы он не перемещаться по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d37bc-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="d37bc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d37bc-105">**Value**</span></span>|<span data-ttu-id="d37bc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d37bc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d37bc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d37bc-107">TRUE</span></span>  <br/> | <span data-ttu-id="d37bc-108">Позиция по горизонтали блокировки.</span><span class="sxs-lookup"><span data-stu-id="d37bc-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="d37bc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d37bc-109">FALSE</span></span>  <br/> | <span data-ttu-id="d37bc-110">Позиция по горизонтали не блокируется.</span><span class="sxs-lookup"><span data-stu-id="d37bc-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d37bc-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d37bc-111">Remarks</span></span>

<span data-ttu-id="d37bc-112">Чтобы получить ссылку на ячейку LockMoveX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d37bc-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d37bc-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d37bc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d37bc-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="d37bc-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="d37bc-115">Для получения ссылки на ячейки LockMoveX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d37bc-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d37bc-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d37bc-116">Section index:</span></span>  <br/> |<span data-ttu-id="d37bc-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d37bc-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d37bc-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d37bc-118">Row index:</span></span>  <br/> |<span data-ttu-id="d37bc-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d37bc-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d37bc-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d37bc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d37bc-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="d37bc-121">**visLockMoveX**</span></span> <br/> |
   

