---
title: EventMultiDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337193"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="3046e-102">EventMultiDrop Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="3046e-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="3046e-103">Ячейка события, вычисляемая при разрыве нескольких фигур на странице документа либо в виде экземпляров, либо при копировании или вставке фигур.</span><span class="sxs-lookup"><span data-stu-id="3046e-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="3046e-104">Ячейки событий оцениваются только при возникновении события, а не при вводе формул.</span><span class="sxs-lookup"><span data-stu-id="3046e-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="3046e-105">Чтобы сослаться на ячейку EventMultiDrop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="3046e-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3046e-106">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3046e-106">Cell name:</span></span>  <br/> |<span data-ttu-id="3046e-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="3046e-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="3046e-108">Чтобы сослаться на ячейку EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3046e-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3046e-109">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3046e-109">Section index:</span></span>  <br/> |<span data-ttu-id="3046e-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3046e-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3046e-111">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3046e-111">Row index:</span></span>  <br/> |<span data-ttu-id="3046e-112">**Висровевент**</span><span class="sxs-lookup"><span data-stu-id="3046e-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="3046e-113">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3046e-113">Cell index:</span></span>  <br/> |<span data-ttu-id="3046e-114">**Висевтцеллмултидроп**</span><span class="sxs-lookup"><span data-stu-id="3046e-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

