---
title: LockHeight Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Блокирует высоту фигуры, чтобы ее высота оставалась неизменной при изменениях размера фигуры.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432088"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="e2949-103">LockHeight Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="e2949-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="e2949-104">Блокирует высоту фигуры, чтобы ее высота оставалась неизменной при изменениях размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="e2949-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="e2949-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e2949-105">**Value**</span></span>|<span data-ttu-id="e2949-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2949-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e2949-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e2949-107">TRUE</span></span>  <br/> | <span data-ttu-id="e2949-108">Высота заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e2949-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="e2949-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e2949-109">FALSE</span></span>  <br/> | <span data-ttu-id="e2949-110">Высота не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e2949-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2949-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2949-111">Remarks</span></span>

<span data-ttu-id="e2949-112">Чтобы получить ссылку на ячейку LockHeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e2949-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2949-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e2949-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e2949-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="e2949-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="e2949-115">Чтобы получить ссылку на ячейку LockHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e2949-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2949-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e2949-116">Section index:</span></span>  <br/> |<span data-ttu-id="e2949-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2949-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e2949-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e2949-118">Row index:</span></span>  <br/> |<span data-ttu-id="e2949-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e2949-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e2949-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e2949-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e2949-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="e2949-121">**visLockHeight**</span></span> <br/> |
   

