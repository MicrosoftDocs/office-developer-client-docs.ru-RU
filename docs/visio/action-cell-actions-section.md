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
description: Содержит формулу, которая должна выполняться, когда пользователь выбирает команду в контекстном меню или меню тегов действий.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283067"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="e352d-103">Action Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="e352d-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="e352d-104">Содержит формулу, которая должна выполняться, когда пользователь выбирает команду в контекстном меню или меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="e352d-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e352d-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="e352d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e352d-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="e352d-106">Remarks</span></span>

<span data-ttu-id="e352d-107">Ячейка Action оценивается только при возникновении действия, а не при вводе формулы.</span><span class="sxs-lookup"><span data-stu-id="e352d-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="e352d-108">Чтобы получить ссылку на ячейку Action по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e352d-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e352d-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e352d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e352d-110">Действия.</span><span class="sxs-lookup"><span data-stu-id="e352d-110">Actions.</span></span>  <span data-ttu-id="e352d-111">*Name (имя* ). Действие, в котором выполняются действия.</span><span class="sxs-lookup"><span data-stu-id="e352d-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="e352d-112">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="e352d-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="e352d-113">Чтобы получить ссылку на ячейку действия Сесе по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e352d-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e352d-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e352d-114">Section index:</span></span>  <br/> |<span data-ttu-id="e352d-115">**Виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="e352d-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="e352d-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e352d-116">Row index:</span></span>  <br/> |<span data-ttu-id="e352d-117">**висровактион** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e352d-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e352d-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e352d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e352d-119">**Висактионактион**</span><span class="sxs-lookup"><span data-stu-id="e352d-119">**visActionAction**</span></span> <br/> |
   

