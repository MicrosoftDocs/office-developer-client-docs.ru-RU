---
title: Ячейка EventDblClick (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Ячейка события, которое вычисляется при двойном щелчке фигуры.
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813700"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="4c503-103">Ячейка EventDblClick (раздел "События")</span><span class="sxs-lookup"><span data-stu-id="4c503-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="4c503-104">Ячейка события, которое вычисляется при двойном щелчке фигуры.</span><span class="sxs-lookup"><span data-stu-id="4c503-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c503-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="4c503-105">Remarks</span></span>

<span data-ttu-id="4c503-106">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="4c503-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="4c503-107">Чтобы получить ссылку на ячейку EventDblClick по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c503-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c503-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4c503-108">Cell name:</span></span>  <br/> | <span data-ttu-id="4c503-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="4c503-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="4c503-110">Для получения ссылки на ячейки EventDblClick по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4c503-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c503-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4c503-111">Section index:</span></span>  <br/> |<span data-ttu-id="4c503-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4c503-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4c503-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4c503-113">Row index:</span></span>  <br/> |<span data-ttu-id="4c503-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="4c503-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="4c503-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4c503-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4c503-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="4c503-116">**visEvtCellDblClick**</span></span> <br/> |
   

