---
title: LockVtxEdit Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Блокирует вершины фигуры таким образом, чтобы они не могли быть изменены.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417668"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="2a6df-103">LockVtxEdit Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="2a6df-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="2a6df-104">Блокирует вершины фигуры таким образом, чтобы они не могли быть изменены.</span><span class="sxs-lookup"><span data-stu-id="2a6df-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="2a6df-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2a6df-105">**Value**</span></span>|<span data-ttu-id="2a6df-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a6df-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a6df-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a6df-107">TRUE</span></span>  <br/> |<span data-ttu-id="2a6df-108">Вершины не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="2a6df-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="2a6df-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a6df-109">FALSE</span></span>  <br/> |<span data-ttu-id="2a6df-110">Вершины можно изменить.</span><span class="sxs-lookup"><span data-stu-id="2a6df-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a6df-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="2a6df-111">Remarks</span></span>

<span data-ttu-id="2a6df-112">Чтобы получить ссылку на ячейку LockVtxEdit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2a6df-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a6df-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2a6df-113">Cell name:</span></span>  <br/> |<span data-ttu-id="2a6df-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="2a6df-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="2a6df-115">Чтобы получить ссылку на ячейку LockVtxEdit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2a6df-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a6df-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2a6df-116">Section index:</span></span>  <br/> |<span data-ttu-id="2a6df-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a6df-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2a6df-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2a6df-118">Row index:</span></span>  <br/> |<span data-ttu-id="2a6df-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2a6df-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="2a6df-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2a6df-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2a6df-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="2a6df-121">**visLockVtxEdit**</span></span> <br/> |
   

