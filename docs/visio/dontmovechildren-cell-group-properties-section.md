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
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="74cf1-103">DontMoveChildren Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="74cf1-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="74cf1-104">Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="74cf1-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="74cf1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="74cf1-105">**Value**</span></span>|<span data-ttu-id="74cf1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74cf1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="74cf1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="74cf1-107">TRUE</span></span>  <br/> | <span data-ttu-id="74cf1-108">Не позволяйте перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="74cf1-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="74cf1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="74cf1-109">FALSE</span></span>  <br/> | <span data-ttu-id="74cf1-110">Разрешить перетаскивание фигур в группе с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="74cf1-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74cf1-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="74cf1-111">Remarks</span></span>

<span data-ttu-id="74cf1-112">Когда значение этой ячейки true, вы все равно можете перевернуть, повернуть, изменить размер или изменить фигуры в группах с помощью других методов.</span><span class="sxs-lookup"><span data-stu-id="74cf1-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="74cf1-113">Значение этой ячейки true для групп в мастерах и группах в экземплярах мастеров, созданных в версиях Visio версии 2000.</span><span class="sxs-lookup"><span data-stu-id="74cf1-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="74cf1-114">Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="74cf1-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74cf1-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="74cf1-115">Cell name:</span></span>  <br/> | <span data-ttu-id="74cf1-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="74cf1-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="74cf1-117">Чтобы получить ссылку на ячейку DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="74cf1-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74cf1-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="74cf1-118">Section index:</span></span>  <br/> |<span data-ttu-id="74cf1-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="74cf1-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="74cf1-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="74cf1-120">Row index:</span></span>  <br/> |<span data-ttu-id="74cf1-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="74cf1-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="74cf1-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="74cf1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="74cf1-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="74cf1-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

