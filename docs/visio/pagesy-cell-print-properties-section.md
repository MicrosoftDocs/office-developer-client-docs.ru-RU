---
title: PagesY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Определяет количество страниц принтера, на которых размещается страница документа по вертикали.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429784"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="580e9-103">PagesY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="580e9-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="580e9-104">Определяет количество страниц принтера, на которых размещается страница документа по вертикали.</span><span class="sxs-lookup"><span data-stu-id="580e9-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="580e9-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="580e9-105">Remarks</span></span>

<span data-ttu-id="580e9-106">Это значение используется только в том случае, если ячейка onPage имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="580e9-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="580e9-107">Чтобы получить ссылку на ячейку страницы по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="580e9-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="580e9-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="580e9-108">Cell name:</span></span>  <br/> | <span data-ttu-id="580e9-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="580e9-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="580e9-110">Чтобы получить ссылку на ячейку Pages по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="580e9-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="580e9-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="580e9-111">Section index:</span></span>  <br/> |<span data-ttu-id="580e9-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="580e9-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="580e9-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="580e9-113">Row index:</span></span>  <br/> |<span data-ttu-id="580e9-114">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="580e9-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="580e9-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="580e9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="580e9-116">**Виспринтпропертиеспажеси**</span><span class="sxs-lookup"><span data-stu-id="580e9-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

