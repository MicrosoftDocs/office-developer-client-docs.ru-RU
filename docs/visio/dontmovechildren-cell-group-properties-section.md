---
title: Ячейка DontMoveChildren (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Определяет, будет ли перетаскивать фигуры в группы с помощью мыши.
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813634"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="debfe-103">Ячейка DontMoveChildren (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="debfe-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="debfe-104">Определяет, будет ли перетаскивать фигуры в группы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="debfe-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="debfe-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="debfe-105">**Value**</span></span>|<span data-ttu-id="debfe-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="debfe-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="debfe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="debfe-107">TRUE</span></span>  <br/> | <span data-ttu-id="debfe-108">Не разрешать фигур в группе для переноса с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="debfe-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="debfe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="debfe-109">FALSE</span></span>  <br/> | <span data-ttu-id="debfe-110">Разрешить фигур в группе для переноса с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="debfe-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="debfe-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="debfe-111">Remarks</span></span>

<span data-ttu-id="debfe-112">Когда значение ячейки имеет значение TRUE, можно по-прежнему отражение, поворот, изменения размера или изменить положение фигур в группы, используя другие методы.</span><span class="sxs-lookup"><span data-stu-id="debfe-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="debfe-113">Значение ячейки имеет значение TRUE для групп в образцов и групп в экземпляры образцов, созданных в версиях Visio до версии 2000.</span><span class="sxs-lookup"><span data-stu-id="debfe-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="debfe-114">Чтобы получить ссылку на ячейку DontMoveChildren по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="debfe-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="debfe-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="debfe-115">Cell name:</span></span>  <br/> | <span data-ttu-id="debfe-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="debfe-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="debfe-117">Для получения ссылки на ячейки DontMoveChildren по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="debfe-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="debfe-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="debfe-118">Section index:</span></span>  <br/> |<span data-ttu-id="debfe-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="debfe-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="debfe-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="debfe-120">Row index:</span></span>  <br/> |<span data-ttu-id="debfe-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="debfe-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="debfe-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="debfe-122">Cell index:</span></span>  <br/> |<span data-ttu-id="debfe-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="debfe-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

