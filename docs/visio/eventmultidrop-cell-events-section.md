---
title: Ячейка EventMultiDrop (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813715"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="5ff86-102">Ячейка EventMultiDrop (раздел "События")</span><span class="sxs-lookup"><span data-stu-id="5ff86-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="5ff86-103">Ячейка события, которое оценивается при перетаскивании нескольких фигур на странице документа в виде экземпляров или при дублировании или вставке фигур.</span><span class="sxs-lookup"><span data-stu-id="5ff86-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="5ff86-104">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="5ff86-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="5ff86-105">Для ссылки на ячейки EventMultiDrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5ff86-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ff86-106">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5ff86-106">Cell name:</span></span>  <br/> |<span data-ttu-id="5ff86-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="5ff86-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="5ff86-108">Для ссылки на ячейки EventMultiDrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5ff86-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ff86-109">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5ff86-109">Section index:</span></span>  <br/> |<span data-ttu-id="5ff86-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ff86-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5ff86-111">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5ff86-111">Row index:</span></span>  <br/> |<span data-ttu-id="5ff86-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="5ff86-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="5ff86-113">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5ff86-113">Cell index:</span></span>  <br/> |<span data-ttu-id="5ff86-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="5ff86-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

