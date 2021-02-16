---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Определяет, можно ли изменить вариант темы, примененный к странице или фигуре, в качестве boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427929"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="47e30-103">LockVariation Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="47e30-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="47e30-104">Определяет, можно ли изменить вариант темы, примененный к странице или фигуре, в качестве boolean.</span><span class="sxs-lookup"><span data-stu-id="47e30-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47e30-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="47e30-105">TRUE</span></span>  <br/> |<span data-ttu-id="47e30-106">Текущий вариант, примененный к странице или фигуре, изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="47e30-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="47e30-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="47e30-107">FALSE</span></span>  <br/> |<span data-ttu-id="47e30-108">Вариант страницы или фигуры можно изменить.</span><span class="sxs-lookup"><span data-stu-id="47e30-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47e30-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="47e30-109">Remarks</span></span>

<span data-ttu-id="47e30-110">Чтобы получить ссылку на ячейку **LockVariation** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="47e30-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47e30-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="47e30-111">Cell name:</span></span>  <br/> | <span data-ttu-id="47e30-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="47e30-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="47e30-113">Чтобы получить ссылку на ячейку **LockVariation** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="47e30-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47e30-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="47e30-114">Section index:</span></span>  <br/> |<span data-ttu-id="47e30-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="47e30-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="47e30-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="47e30-116">Row index:</span></span>  <br/> |<span data-ttu-id="47e30-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="47e30-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="47e30-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="47e30-118">Cell index:</span></span>  <br/> |<span data-ttu-id="47e30-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="47e30-119">**visLockVariation**</span></span> <br/> |
   

