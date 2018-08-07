---
title: Ячейка EventDrop (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Ячейка события, которое оценивается при перетаскивании фигуры на странице документа как экземпляр или при дублировании или вставке фигуры.
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813698"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="54ba1-103">Ячейка EventDrop (раздел "События")</span><span class="sxs-lookup"><span data-stu-id="54ba1-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="54ba1-104">Ячейка события, которое оценивается при перетаскивании фигуры на странице документа как экземпляр или при дублировании или вставке фигуры.</span><span class="sxs-lookup"><span data-stu-id="54ba1-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54ba1-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="54ba1-105">Remarks</span></span>

<span data-ttu-id="54ba1-106">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="54ba1-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="54ba1-107">Чтобы получить ссылку на ячейку EventDrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54ba1-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54ba1-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="54ba1-108">Cell name:</span></span>  <br/> | <span data-ttu-id="54ba1-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="54ba1-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="54ba1-110">Для получения ссылки на ячейки EventDrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="54ba1-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54ba1-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="54ba1-111">Section index:</span></span>  <br/> |<span data-ttu-id="54ba1-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54ba1-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54ba1-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="54ba1-113">Row index:</span></span>  <br/> |<span data-ttu-id="54ba1-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="54ba1-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="54ba1-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="54ba1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="54ba1-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="54ba1-116">**visEvtCellDrop**</span></span> <br/> |
   

