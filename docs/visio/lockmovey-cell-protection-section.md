---
title: Ячейка LockMoveY (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Блокирует вертикальную позицию фигуры, чтобы он не перемещаться по вертикали.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814136"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="a1c6a-103">Ячейка LockMoveY (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="a1c6a-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="a1c6a-104">Блокирует вертикальную позицию фигуры, чтобы он не перемещаться по вертикали.</span><span class="sxs-lookup"><span data-stu-id="a1c6a-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="a1c6a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a1c6a-105">**Value**</span></span>|<span data-ttu-id="a1c6a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1c6a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a1c6a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1c6a-107">TRUE</span></span>  <br/> | <span data-ttu-id="a1c6a-108">Позиция по вертикали блокировки.</span><span class="sxs-lookup"><span data-stu-id="a1c6a-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="a1c6a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1c6a-109">FALSE</span></span>  <br/> | <span data-ttu-id="a1c6a-110">Позиция по вертикали не блокируется.</span><span class="sxs-lookup"><span data-stu-id="a1c6a-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1c6a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1c6a-111">Remarks</span></span>

<span data-ttu-id="a1c6a-112">Чтобы получить ссылку на ячейку LockMoveY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a1c6a-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1c6a-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a1c6a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a1c6a-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="a1c6a-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="a1c6a-115">Для получения ссылки на ячейки LockMoveY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a1c6a-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1c6a-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a1c6a-116">Section index:</span></span>  <br/> |<span data-ttu-id="a1c6a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1c6a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a1c6a-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a1c6a-118">Row index:</span></span>  <br/> |<span data-ttu-id="a1c6a-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a1c6a-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a1c6a-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a1c6a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a1c6a-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="a1c6a-121">**visLockMoveY**</span></span> <br/> |
   

