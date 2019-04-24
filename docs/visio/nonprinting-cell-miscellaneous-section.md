---
title: NonPrinting Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Включает и выключает печать для выбранной фигуры.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357234"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="ba88d-103">NonPrinting Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="ba88d-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ba88d-104">Включает и выключает печать для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="ba88d-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="ba88d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ba88d-105">**Value**</span></span>|<span data-ttu-id="ba88d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ba88d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ba88d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ba88d-107">TRUE</span></span>  <br/> | <span data-ttu-id="ba88d-108">Печать отключена, но фигура будет отображаться в окне документа.</span><span class="sxs-lookup"><span data-stu-id="ba88d-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="ba88d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ba88d-109">FALSE</span></span>  <br/> | <span data-ttu-id="ba88d-110">Печать включена.</span><span class="sxs-lookup"><span data-stu-id="ba88d-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba88d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba88d-111">Remarks</span></span>

<span data-ttu-id="ba88d-112">Вы можете напечатать направляющую, выбрав ее, а затем присвоив неПечатаемой ячейке значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="ba88d-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="ba88d-113">Чтобы получить ссылку на неПечатаемую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="ba88d-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba88d-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ba88d-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ba88d-115">NonPrinting</span><span class="sxs-lookup"><span data-stu-id="ba88d-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="ba88d-116">Чтобы получить ссылку на неПечатаемую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ba88d-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba88d-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ba88d-117">Section index:</span></span>  <br/> |<span data-ttu-id="ba88d-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ba88d-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ba88d-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ba88d-119">Row index:</span></span>  <br/> |<span data-ttu-id="ba88d-120">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="ba88d-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ba88d-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ba88d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ba88d-122">**Виснонпринтинг**</span><span class="sxs-lookup"><span data-stu-id="ba88d-122">**visNonPrinting**</span></span> <br/> |
   

