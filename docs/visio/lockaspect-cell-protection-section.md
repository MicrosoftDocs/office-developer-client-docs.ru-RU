---
title: LockAspect Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Блокирует пропорции фигуры таким образом, чтобы ее можно было изменять только пропорционально. его нельзя изменять в отдельном измерении.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411584"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="e8dc3-103">LockAspect Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="e8dc3-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="e8dc3-104">Блокирует пропорции фигуры таким образом, чтобы ее можно было изменять только пропорционально. его нельзя изменять в отдельном измерении.</span><span class="sxs-lookup"><span data-stu-id="e8dc3-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="e8dc3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e8dc3-105">**Value**</span></span>|<span data-ttu-id="e8dc3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8dc3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e8dc3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8dc3-107">TRUE</span></span>  <br/> | <span data-ttu-id="e8dc3-108">Пропорции заблокированы.</span><span class="sxs-lookup"><span data-stu-id="e8dc3-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="e8dc3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8dc3-109">FALSE</span></span>  <br/> | <span data-ttu-id="e8dc3-110">Пропорции не блокируются.</span><span class="sxs-lookup"><span data-stu-id="e8dc3-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8dc3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8dc3-111">Remarks</span></span>

<span data-ttu-id="e8dc3-112">Чтобы получить ссылку на ячейку LockAspect по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dc3-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e8dc3-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="e8dc3-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="e8dc3-115">Чтобы получить ссылку на ячейку LockAspect по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dc3-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-116">Section index:</span></span>  <br/> |<span data-ttu-id="e8dc3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8dc3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8dc3-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-118">Row index:</span></span>  <br/> |<span data-ttu-id="e8dc3-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="e8dc3-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e8dc3-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8dc3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e8dc3-121">**Вислоккаспект**</span><span class="sxs-lookup"><span data-stu-id="e8dc3-121">**visLockAspect**</span></span> <br/> |
   

