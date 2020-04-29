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
description: Блокирует ширину фигуры таким образом, чтобы ее ширина оставалась неизменной при изменении размера фигуры.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439809"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="0fe1a-103">LockWidth Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="0fe1a-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="0fe1a-104">Блокирует ширину фигуры таким образом, чтобы ее ширина оставалась неизменной при изменении размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="0fe1a-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="0fe1a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0fe1a-105">**Value**</span></span>|<span data-ttu-id="0fe1a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0fe1a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0fe1a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fe1a-107">TRUE</span></span>  <br/> | <span data-ttu-id="0fe1a-108">Ширина заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0fe1a-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="0fe1a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0fe1a-109">FALSE</span></span>  <br/> | <span data-ttu-id="0fe1a-110">Ширина не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0fe1a-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fe1a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fe1a-111">Remarks</span></span>

<span data-ttu-id="0fe1a-112">Чтобы получить ссылку на ячейку LockWidth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fe1a-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0fe1a-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="0fe1a-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="0fe1a-115">Чтобы получить ссылку на ячейку LockWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fe1a-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-116">Section index:</span></span>  <br/> |<span data-ttu-id="0fe1a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0fe1a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0fe1a-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-118">Row index:</span></span>  <br/> |<span data-ttu-id="0fe1a-119">**висровлокк**</span><span class="sxs-lookup"><span data-stu-id="0fe1a-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="0fe1a-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0fe1a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0fe1a-121">**вислокквидс**</span><span class="sxs-lookup"><span data-stu-id="0fe1a-121">**visLockWidth**</span></span> <br/> |
   

