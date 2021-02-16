---
title: EventXFMod Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Ячейка события, которая оценивается при преобразовании положения или ориентации фигуры на странице (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418535"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="5bff4-103">EventXFMod Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="5bff4-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="5bff4-104">Ячейка события, которая оценивается при преобразовании положения или ориентации фигуры на странице ("XF").</span><span class="sxs-lookup"><span data-stu-id="5bff4-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bff4-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5bff4-105">Remarks</span></span>

<span data-ttu-id="5bff4-106">Ячейки событий оцениваются только при событии, а не при вводе формулы.</span><span class="sxs-lookup"><span data-stu-id="5bff4-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="5bff4-107">Чтобы получить ссылку на ячейку EventXFMod по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5bff4-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bff4-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bff4-108">Cell name:</span></span>  <br/> | <span data-ttu-id="5bff4-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="5bff4-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="5bff4-110">Чтобы получить ссылку на ячейку EventXFMod по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5bff4-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bff4-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5bff4-111">Section index:</span></span>  <br/> |<span data-ttu-id="5bff4-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5bff4-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5bff4-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5bff4-113">Row index:</span></span>  <br/> |<span data-ttu-id="5bff4-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="5bff4-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="5bff4-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bff4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5bff4-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="5bff4-116">**visEvtCellXFMod**</span></span> <br/> |
   

