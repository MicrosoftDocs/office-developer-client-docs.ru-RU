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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416596"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="2bddc-103">DontMoveChildren Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2bddc-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="2bddc-104">Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="2bddc-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="2bddc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2bddc-105">**Value**</span></span>|<span data-ttu-id="2bddc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2bddc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2bddc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2bddc-107">TRUE</span></span>  <br/> | <span data-ttu-id="2bddc-108">Не разрешать перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="2bddc-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="2bddc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2bddc-109">FALSE</span></span>  <br/> | <span data-ttu-id="2bddc-110">Разрешить перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="2bddc-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bddc-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="2bddc-111">Remarks</span></span>

<span data-ttu-id="2bddc-112">Если ячейка имеет значение TRUE, вы по-прежнему можете отражать, поворачивать, изменять размер и положение фигур в группах, используя другие методы.</span><span class="sxs-lookup"><span data-stu-id="2bddc-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="2bddc-113">Значение этой ячейки равно TRUE для групп в шаблонах и группах в экземплярах образцов, созданных в версиях Visio до версии 2000.</span><span class="sxs-lookup"><span data-stu-id="2bddc-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="2bddc-114">Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2bddc-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2bddc-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2bddc-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2bddc-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="2bddc-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="2bddc-117">Чтобы получить ссылку на ячейку DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2bddc-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2bddc-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2bddc-118">Section index:</span></span>  <br/> |<span data-ttu-id="2bddc-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2bddc-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2bddc-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2bddc-120">Row index:</span></span>  <br/> |<span data-ttu-id="2bddc-121">**Висровграуп**</span><span class="sxs-lookup"><span data-stu-id="2bddc-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="2bddc-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2bddc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2bddc-123">**Висграупдонтмовечилдрен**</span><span class="sxs-lookup"><span data-stu-id="2bddc-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

