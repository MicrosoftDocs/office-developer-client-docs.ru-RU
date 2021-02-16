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
description: Предотвращает выбор фигуры.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409757"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="ffb06-103">LockSelect Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="ffb06-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="ffb06-104">Предотвращает выбор фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffb06-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="ffb06-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ffb06-105">**Value**</span></span>|<span data-ttu-id="ffb06-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffb06-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ffb06-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ffb06-107">TRUE</span></span>  <br/> | <span data-ttu-id="ffb06-108">Не удается выбрать фигуру.</span><span class="sxs-lookup"><span data-stu-id="ffb06-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="ffb06-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ffb06-109">FALSE</span></span>  <br/> | <span data-ttu-id="ffb06-110">Фигуру можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="ffb06-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffb06-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ffb06-111">Remarks</span></span>

<span data-ttu-id="ffb06-112">Чтобы lockSelect вступил в силу, в диалоговом окне "Защита документа" должен быть выбран соответствующий контроль.  </span><span class="sxs-lookup"><span data-stu-id="ffb06-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="ffb06-113">Чтобы получить ссылку на ячейку LockSelect по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ffb06-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffb06-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ffb06-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ffb06-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="ffb06-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="ffb06-116">Чтобы получить ссылку на ячейку LockSelect по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ffb06-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffb06-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ffb06-117">Section index:</span></span>  <br/> |<span data-ttu-id="ffb06-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ffb06-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ffb06-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ffb06-119">Row index:</span></span>  <br/> |<span data-ttu-id="ffb06-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ffb06-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ffb06-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ffb06-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ffb06-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="ffb06-122">**visLockSelect**</span></span> <br/> |
   

