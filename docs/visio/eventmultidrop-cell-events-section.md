---
title: EventMultiDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416722"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="76e8e-102">EventMultiDrop Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="76e8e-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="76e8e-103">Ячейка событий, которая оценивается при сбросе нескольких фигур на страницу рисования, как экземпляры, так и когда фигуры дублируются или вклеяются.</span><span class="sxs-lookup"><span data-stu-id="76e8e-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="76e8e-104">Ячейки событий оцениваются только при событии, а не при входе формулы.</span><span class="sxs-lookup"><span data-stu-id="76e8e-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="76e8e-105">Чтобы сослаться на ячейку EventMultiDrop по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="76e8e-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76e8e-106">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="76e8e-106">Cell name:</span></span>  <br/> |<span data-ttu-id="76e8e-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="76e8e-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="76e8e-108">Чтобы сослаться на ячейку EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="76e8e-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76e8e-109">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="76e8e-109">Section index:</span></span>  <br/> |<span data-ttu-id="76e8e-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="76e8e-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="76e8e-111">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="76e8e-111">Row index:</span></span>  <br/> |<span data-ttu-id="76e8e-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="76e8e-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="76e8e-113">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="76e8e-113">Cell index:</span></span>  <br/> |<span data-ttu-id="76e8e-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="76e8e-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

