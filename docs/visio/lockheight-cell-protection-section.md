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
description: Блокирует высоту фигуры таким образом, что ее высота остается неизменной при изменении размера фигуры.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341778"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="6e4b2-103">LockHeight Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="6e4b2-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="6e4b2-104">Блокирует высоту фигуры таким образом, что ее высота остается неизменной при изменении размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="6e4b2-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="6e4b2-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6e4b2-105">**Value**</span></span>|<span data-ttu-id="6e4b2-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e4b2-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6e4b2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6e4b2-107">TRUE</span></span>  <br/> | <span data-ttu-id="6e4b2-108">Высота заблокирована.</span><span class="sxs-lookup"><span data-stu-id="6e4b2-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="6e4b2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6e4b2-109">FALSE</span></span>  <br/> | <span data-ttu-id="6e4b2-110">Высота не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="6e4b2-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e4b2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e4b2-111">Remarks</span></span>

<span data-ttu-id="6e4b2-112">Чтобы получить ссылку на ячейку LockHeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e4b2-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6e4b2-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="6e4b2-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="6e4b2-115">Чтобы получить ссылку на ячейку LockHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e4b2-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-116">Section index:</span></span>  <br/> |<span data-ttu-id="6e4b2-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6e4b2-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6e4b2-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-118">Row index:</span></span>  <br/> |<span data-ttu-id="6e4b2-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="6e4b2-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6e4b2-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6e4b2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6e4b2-121">**Вислоккхеигхт**</span><span class="sxs-lookup"><span data-stu-id="6e4b2-121">**visLockHeight**</span></span> <br/> |
   

