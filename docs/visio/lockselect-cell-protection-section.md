---
title: LockSelect Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Запрещает выбор фигуры.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360671"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="05020-103">LockSelect Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="05020-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="05020-104">Запрещает выбор фигуры.</span><span class="sxs-lookup"><span data-stu-id="05020-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="05020-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="05020-105">**Value**</span></span>|<span data-ttu-id="05020-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05020-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="05020-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="05020-107">TRUE</span></span>  <br/> | <span data-ttu-id="05020-108">Невозможно выбрать фигуру.</span><span class="sxs-lookup"><span data-stu-id="05020-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="05020-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="05020-109">FALSE</span></span>  <br/> | <span data-ttu-id="05020-110">Можно выбрать фигуру.</span><span class="sxs-lookup"><span data-stu-id="05020-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05020-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="05020-111">Remarks</span></span>

<span data-ttu-id="05020-112">Чтобы LockSelect вступили в силу, в диалоговом окне **Защита документа** должен быть установлен флажок **фигуры** .</span><span class="sxs-lookup"><span data-stu-id="05020-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="05020-113">Чтобы получить ссылку на ячейку LockSelect по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="05020-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05020-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="05020-114">Cell name:</span></span>  <br/> | <span data-ttu-id="05020-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="05020-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="05020-116">Чтобы получить ссылку на ячейку LockSelect по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="05020-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05020-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="05020-117">Section index:</span></span>  <br/> |<span data-ttu-id="05020-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05020-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05020-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="05020-119">Row index:</span></span>  <br/> |<span data-ttu-id="05020-120">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="05020-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="05020-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="05020-121">Cell index:</span></span>  <br/> |<span data-ttu-id="05020-122">**Вислоккселект**</span><span class="sxs-lookup"><span data-stu-id="05020-122">**visLockSelect**</span></span> <br/> |
   

