---
title: LockBegin Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Блокирует начальную точку (BeginX, начало) фигуры 1-D в определенном расположении.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359649"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="b6e2e-103">LockBegin Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="b6e2e-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="b6e2e-104">Блокирует начальную точку (BeginX, начало) фигуры 1-D в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="b6e2e-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="b6e2e-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b6e2e-105">**Value**</span></span>|<span data-ttu-id="b6e2e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6e2e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b6e2e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b6e2e-107">TRUE</span></span>  <br/> | <span data-ttu-id="b6e2e-108">Начальная точка заблокирована.</span><span class="sxs-lookup"><span data-stu-id="b6e2e-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="b6e2e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6e2e-109">FALSE</span></span>  <br/> | <span data-ttu-id="b6e2e-110">Начало не заблокировано.</span><span class="sxs-lookup"><span data-stu-id="b6e2e-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6e2e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6e2e-111">Remarks</span></span>

<span data-ttu-id="b6e2e-112">Чтобы получить ссылку на ячейку LockBegin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e2e-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b6e2e-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="b6e2e-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="b6e2e-115">Чтобы получить ссылку на ячейку LockBegin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e2e-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-116">Section index:</span></span>  <br/> |<span data-ttu-id="b6e2e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6e2e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6e2e-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-118">Row index:</span></span>  <br/> |<span data-ttu-id="b6e2e-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="b6e2e-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b6e2e-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6e2e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b6e2e-121">**Вислоккбегин**</span><span class="sxs-lookup"><span data-stu-id="b6e2e-121">**visLockBegin**</span></span> <br/> |
   

