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
description: Блокирует точку начала (BeginX, BeginY) формы 1-D в определенное расположение.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407762"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="b9943-103">LockBegin Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="b9943-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="b9943-104">Блокирует точку начала (BeginX, BeginY) формы 1-D в определенное расположение.</span><span class="sxs-lookup"><span data-stu-id="b9943-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="b9943-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b9943-105">**Value**</span></span>|<span data-ttu-id="b9943-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9943-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b9943-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9943-107">TRUE</span></span>  <br/> | <span data-ttu-id="b9943-108">Точка начала заблокирована.</span><span class="sxs-lookup"><span data-stu-id="b9943-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="b9943-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9943-109">FALSE</span></span>  <br/> | <span data-ttu-id="b9943-110">Начало не заблокировано.</span><span class="sxs-lookup"><span data-stu-id="b9943-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9943-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9943-111">Remarks</span></span>

<span data-ttu-id="b9943-112">Чтобы получить ссылку на ячейку LockBegin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b9943-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9943-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b9943-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b9943-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="b9943-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="b9943-115">Чтобы получить ссылку на ячейку LockBegin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b9943-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9943-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b9943-116">Section index:</span></span>  <br/> |<span data-ttu-id="b9943-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9943-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b9943-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b9943-118">Row index:</span></span>  <br/> |<span data-ttu-id="b9943-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b9943-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b9943-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b9943-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b9943-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="b9943-121">**visLockBegin**</span></span> <br/> |
   

