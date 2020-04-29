---
title: EventDblClick Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Ячейка события, вычисляемая при двойном щелчке фигуры.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438220"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="cc3a3-103">EventDblClick Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="cc3a3-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="cc3a3-104">Ячейка события, вычисляемая при двойном щелчке фигуры.</span><span class="sxs-lookup"><span data-stu-id="cc3a3-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc3a3-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc3a3-105">Remarks</span></span>

<span data-ttu-id="cc3a3-106">Ячейки событий оцениваются только при возникновении события, а не при вводе формул.</span><span class="sxs-lookup"><span data-stu-id="cc3a3-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="cc3a3-107">Чтобы получить ссылку на ячейку EventDblClick по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc3a3-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cc3a3-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="cc3a3-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="cc3a3-110">Чтобы получить ссылку на ячейку EventDblClick по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc3a3-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-111">Section index:</span></span>  <br/> |<span data-ttu-id="cc3a3-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc3a3-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cc3a3-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-113">Row index:</span></span>  <br/> |<span data-ttu-id="cc3a3-114">**висровевент**</span><span class="sxs-lookup"><span data-stu-id="cc3a3-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="cc3a3-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc3a3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cc3a3-116">**висевтцеллдблкликк**</span><span class="sxs-lookup"><span data-stu-id="cc3a3-116">**visEvtCellDblClick**</span></span> <br/> |
   

