---
title: Ячейка LockSelect (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Запрещает выбранной фигуры.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814157"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="e05f6-103">Ячейка LockSelect (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="e05f6-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="e05f6-104">Запрещает выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="e05f6-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="e05f6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e05f6-105">**Value**</span></span>|<span data-ttu-id="e05f6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e05f6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e05f6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e05f6-107">TRUE</span></span>  <br/> | <span data-ttu-id="e05f6-108">Невозможно выбрать фигуры.</span><span class="sxs-lookup"><span data-stu-id="e05f6-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="e05f6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e05f6-109">FALSE</span></span>  <br/> | <span data-ttu-id="e05f6-110">Можно выбирать фигуры.</span><span class="sxs-lookup"><span data-stu-id="e05f6-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e05f6-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="e05f6-111">Remarks</span></span>

<span data-ttu-id="e05f6-112">Чтобы LockSelect вступили в силу необходимо выбрать флажок **фигур** в диалоговом окне **Защита документа** .</span><span class="sxs-lookup"><span data-stu-id="e05f6-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="e05f6-113">Чтобы получить ссылку на ячейку LockSelect по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e05f6-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e05f6-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e05f6-114">Cell name:</span></span>  <br/> | <span data-ttu-id="e05f6-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="e05f6-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="e05f6-116">Для получения ссылки на ячейки LockSelect по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e05f6-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e05f6-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e05f6-117">Section index:</span></span>  <br/> |<span data-ttu-id="e05f6-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e05f6-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e05f6-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e05f6-119">Row index:</span></span>  <br/> |<span data-ttu-id="e05f6-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e05f6-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e05f6-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e05f6-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e05f6-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="e05f6-122">**visLockSelect**</span></span> <br/> |
   

