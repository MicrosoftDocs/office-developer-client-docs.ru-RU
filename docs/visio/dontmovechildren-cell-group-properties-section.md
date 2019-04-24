---
title: DontMoveChildren Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338586"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="ca059-103">DontMoveChildren Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ca059-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="ca059-104">Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ca059-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="ca059-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ca059-105">**Value**</span></span>|<span data-ttu-id="ca059-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca059-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ca059-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca059-107">TRUE</span></span>  <br/> | <span data-ttu-id="ca059-108">Не разрешать перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ca059-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="ca059-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca059-109">FALSE</span></span>  <br/> | <span data-ttu-id="ca059-110">Разрешить перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ca059-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca059-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca059-111">Remarks</span></span>

<span data-ttu-id="ca059-112">Если ячейка имеет значение TRUE, вы по-прежнему можете отражать, поворачивать, изменять размер и положение фигур в группах, используя другие методы.</span><span class="sxs-lookup"><span data-stu-id="ca059-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="ca059-113">Значение этой ячейки равно TRUE для групп в шаблонах и группах в экземплярах образцов, созданных в версиях Visio до версии 2000.</span><span class="sxs-lookup"><span data-stu-id="ca059-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="ca059-114">Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ca059-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca059-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ca059-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ca059-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="ca059-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="ca059-117">Чтобы получить ссылку на ячейку DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ca059-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca059-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ca059-118">Section index:</span></span>  <br/> |<span data-ttu-id="ca059-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca059-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca059-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ca059-120">Row index:</span></span>  <br/> |<span data-ttu-id="ca059-121">**Висровграуп**</span><span class="sxs-lookup"><span data-stu-id="ca059-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="ca059-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ca059-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ca059-123">**Висграупдонтмовечилдрен**</span><span class="sxs-lookup"><span data-stu-id="ca059-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

