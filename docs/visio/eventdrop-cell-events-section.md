---
title: EventDrop Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Ячейка события, вычисляемая при разрыве фигуры на странице документа либо в виде экземпляра, либо при копировании или вставке фигуры.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351011"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="fbb6b-103">EventDrop Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="fbb6b-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="fbb6b-104">Ячейка события, вычисляемая при разрыве фигуры на странице документа либо в виде экземпляра, либо при копировании или вставке фигуры.</span><span class="sxs-lookup"><span data-stu-id="fbb6b-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbb6b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbb6b-105">Remarks</span></span>

<span data-ttu-id="fbb6b-106">Ячейки событий оцениваются только при возникновении события, а не при вводе формул.</span><span class="sxs-lookup"><span data-stu-id="fbb6b-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="fbb6b-107">Чтобы получить ссылку на ячейку EventDrop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbb6b-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="fbb6b-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="fbb6b-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="fbb6b-110">Чтобы получить ссылку на ячейку EventDrop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbb6b-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-111">Section index:</span></span>  <br/> |<span data-ttu-id="fbb6b-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fbb6b-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fbb6b-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-113">Row index:</span></span>  <br/> |<span data-ttu-id="fbb6b-114">**Висровевент**</span><span class="sxs-lookup"><span data-stu-id="fbb6b-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="fbb6b-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbb6b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fbb6b-116">**Висевтцеллдроп**</span><span class="sxs-lookup"><span data-stu-id="fbb6b-116">**visEvtCellDrop**</span></span> <br/> |
   

