---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Определяет тип экспресс-стиля (2-мерный, 1-мерный или соединитель), наследуемого формой.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282581"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="591c1-103">QuickStyleType Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="591c1-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="591c1-104">Определяет тип экспресс-стиля (2-мерный, 1-мерный или соединитель), наследуемого формой.</span><span class="sxs-lookup"><span data-stu-id="591c1-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="591c1-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="591c1-105">**Value**</span></span>|<span data-ttu-id="591c1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="591c1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="591c1-107">нуль</span><span class="sxs-lookup"><span data-stu-id="591c1-107">0</span></span>  <br/> |<span data-ttu-id="591c1-108">Visio выбирает автоматически</span><span class="sxs-lookup"><span data-stu-id="591c1-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="591c1-109">1,1</span><span class="sxs-lookup"><span data-stu-id="591c1-109">1</span></span>  <br/> |<span data-ttu-id="591c1-110">1 измерение</span><span class="sxs-lookup"><span data-stu-id="591c1-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="591c1-111">2</span><span class="sxs-lookup"><span data-stu-id="591c1-111">2</span></span>  <br/> |<span data-ttu-id="591c1-112">2 измерения</span><span class="sxs-lookup"><span data-stu-id="591c1-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="591c1-113">4</span><span class="sxs-lookup"><span data-stu-id="591c1-113">3</span></span>  <br/> |<span data-ttu-id="591c1-114">Connector</span><span class="sxs-lookup"><span data-stu-id="591c1-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="591c1-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="591c1-115">Remarks</span></span>

<span data-ttu-id="591c1-116">Чтобы получить ссылку на ячейку **QuickStyleType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="591c1-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="591c1-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="591c1-117">Cell name:</span></span>  <br/> | <span data-ttu-id="591c1-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="591c1-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="591c1-119">Чтобы получить ссылку на ячейку **QuickStyleType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="591c1-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="591c1-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="591c1-120">Section index:</span></span>  <br/> |<span data-ttu-id="591c1-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="591c1-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="591c1-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="591c1-122">Row index:</span></span>  <br/> |<span data-ttu-id="591c1-123">**Висровкуиккстилепропертиес**</span><span class="sxs-lookup"><span data-stu-id="591c1-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="591c1-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="591c1-124">Cell index:</span></span>  <br/> |<span data-ttu-id="591c1-125">**Вискуиккстилетипе**</span><span class="sxs-lookup"><span data-stu-id="591c1-125">**visQuickStyleType**</span></span> <br/> |
   

