---
title: LockEnd Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Блокирует конечную точку (EndX, Енди) одномерной фигуры в определенном расположении.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425584"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="edc89-103">LockEnd Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="edc89-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="edc89-104">Блокирует конечную точку (EndX, Енди) одномерной фигуры в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="edc89-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="edc89-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="edc89-105">**Value**</span></span>|<span data-ttu-id="edc89-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="edc89-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="edc89-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="edc89-107">TRUE</span></span>  <br/> | <span data-ttu-id="edc89-108">Конечная точка заблокирована.</span><span class="sxs-lookup"><span data-stu-id="edc89-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="edc89-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="edc89-109">FALSE</span></span>  <br/> | <span data-ttu-id="edc89-110">Конечная точка не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="edc89-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edc89-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="edc89-111">Remarks</span></span>

<span data-ttu-id="edc89-112">Чтобы получить ссылку на ячейку LockEnd по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="edc89-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edc89-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="edc89-113">Cell name:</span></span>  <br/> | <span data-ttu-id="edc89-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="edc89-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="edc89-115">Чтобы получить ссылку на ячейку LockEnd по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="edc89-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edc89-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="edc89-116">Section index:</span></span>  <br/> |<span data-ttu-id="edc89-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="edc89-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="edc89-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="edc89-118">Row index:</span></span>  <br/> |<span data-ttu-id="edc89-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="edc89-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="edc89-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="edc89-120">Cell index:</span></span>  <br/> |<span data-ttu-id="edc89-121">**Вислоккенд**</span><span class="sxs-lookup"><span data-stu-id="edc89-121">**visLockEnd**</span></span> <br/> |
   

