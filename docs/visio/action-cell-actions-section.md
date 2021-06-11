---
title: Action Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Содержит формулу, которая будет выполняться, когда пользователь выбирает команду в меню ярлыка или тега действий.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407615"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="e816e-103">Action Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="e816e-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="e816e-104">Содержит формулу, которая будет выполняться, когда пользователь выбирает команду в меню ярлыка или тега действий.</span><span class="sxs-lookup"><span data-stu-id="e816e-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e816e-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="e816e-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e816e-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="e816e-106">Remarks</span></span>

<span data-ttu-id="e816e-107">Ячейка Action оценивается только при действии, а не при вступив в формулу.</span><span class="sxs-lookup"><span data-stu-id="e816e-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="e816e-108">Чтобы получить ссылку на ячейку Action по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e816e-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e816e-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e816e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e816e-110">Действия.</span><span class="sxs-lookup"><span data-stu-id="e816e-110">Actions.</span></span>  <span data-ttu-id="e816e-111">*имя*  . Действие, в котором действия.</span><span class="sxs-lookup"><span data-stu-id="e816e-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="e816e-112">*имя*  — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="e816e-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="e816e-113">Чтобы получить ссылку на ячейку Action по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e816e-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e816e-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e816e-114">Section index:</span></span>  <br/> |<span data-ttu-id="e816e-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="e816e-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="e816e-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e816e-116">Row index:</span></span>  <br/> |<span data-ttu-id="e816e-117">**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="e816e-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e816e-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e816e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e816e-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="e816e-119">**visActionAction**</span></span> <br/> |
   

