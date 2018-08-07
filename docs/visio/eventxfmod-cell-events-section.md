---
title: Ячейка EventXFMod (раздел "События")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Ячейка события, которое вычисляется когда позиции или ориентации на странице фигуры преобразовать (XF).
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813727"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="32397-103">Ячейка EventXFMod (раздел "События")</span><span class="sxs-lookup"><span data-stu-id="32397-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="32397-104">Ячейка события, которое вычисляется когда позиции или ориентации на странице фигуры преобразовать («XF»).</span><span class="sxs-lookup"><span data-stu-id="32397-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32397-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="32397-105">Remarks</span></span>

<span data-ttu-id="32397-106">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="32397-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="32397-107">Чтобы получить ссылку на ячейку EventXFMod по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="32397-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32397-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="32397-108">Cell name:</span></span>  <br/> | <span data-ttu-id="32397-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="32397-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="32397-110">Для получения ссылки на ячейки EventXFMod по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="32397-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32397-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="32397-111">Section index:</span></span>  <br/> |<span data-ttu-id="32397-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="32397-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="32397-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="32397-113">Row index:</span></span>  <br/> |<span data-ttu-id="32397-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="32397-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="32397-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="32397-115">Cell index:</span></span>  <br/> |<span data-ttu-id="32397-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="32397-116">**visEvtCellXFMod**</span></span> <br/> |
   

