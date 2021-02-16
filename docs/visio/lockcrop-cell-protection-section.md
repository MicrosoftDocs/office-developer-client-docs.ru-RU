---
title: LockCrop Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Блокирует объект из другой программы от обрезки средством обрезки.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411857"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="dace0-103">LockCrop Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="dace0-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="dace0-104">Блокирует объект из другой программы от обрезки средством **обрезки.**</span><span class="sxs-lookup"><span data-stu-id="dace0-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="dace0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="dace0-105">**Value**</span></span>|<span data-ttu-id="dace0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dace0-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dace0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dace0-107">TRUE</span></span>  <br/> | <span data-ttu-id="dace0-108">Фигуру невозможно обрезить</span><span class="sxs-lookup"><span data-stu-id="dace0-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="dace0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dace0-109">FALSE</span></span>  <br/> | <span data-ttu-id="dace0-110">Фигура может быть обрезана.</span><span class="sxs-lookup"><span data-stu-id="dace0-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dace0-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="dace0-111">Remarks</span></span>

<span data-ttu-id="dace0-112">Чтобы получить ссылку на ячейку LockCrop по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="dace0-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dace0-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dace0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dace0-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="dace0-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="dace0-115">Чтобы получить ссылку на ячейку LockCrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dace0-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dace0-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dace0-116">Section index:</span></span>  <br/> |<span data-ttu-id="dace0-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dace0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dace0-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dace0-118">Row index:</span></span>  <br/> |<span data-ttu-id="dace0-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="dace0-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="dace0-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dace0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dace0-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="dace0-121">**visLockCrop**</span></span> <br/> |
   

