---
title: LockWidth Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Блокирует ширину фигуры так, чтобы ее ширина оставалась неизменной при размере фигуры.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439809"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="5059b-103">LockWidth Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="5059b-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="5059b-104">Блокирует ширину фигуры так, чтобы ее ширина оставалась неизменной при размере фигуры.</span><span class="sxs-lookup"><span data-stu-id="5059b-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="5059b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5059b-105">**Value**</span></span>|<span data-ttu-id="5059b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5059b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5059b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5059b-107">TRUE</span></span>  <br/> | <span data-ttu-id="5059b-108">Ширина заблокирована.</span><span class="sxs-lookup"><span data-stu-id="5059b-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="5059b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5059b-109">FALSE</span></span>  <br/> | <span data-ttu-id="5059b-110">Ширина не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="5059b-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5059b-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="5059b-111">Remarks</span></span>

<span data-ttu-id="5059b-112">Чтобы получить ссылку на ячейку LockWidth по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5059b-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5059b-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5059b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5059b-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="5059b-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="5059b-115">Чтобы получить ссылку на ячейку LockWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5059b-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5059b-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5059b-116">Section index:</span></span>  <br/> |<span data-ttu-id="5059b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5059b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5059b-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5059b-118">Row index:</span></span>  <br/> |<span data-ttu-id="5059b-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5059b-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="5059b-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5059b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5059b-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="5059b-121">**visLockWidth**</span></span> <br/> |
   

