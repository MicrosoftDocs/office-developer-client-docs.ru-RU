---
title: PagesX Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Определяет количество страниц принтера, на которых размещается страница документа по горизонтали.
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438696"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="cccf5-103">PagesX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="cccf5-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="cccf5-104">Определяет количество страниц принтера, на которых размещается страница документа по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="cccf5-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cccf5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="cccf5-105">Remarks</span></span>

<span data-ttu-id="cccf5-106">Это значение используется только в том случае, если ячейка onPage имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="cccf5-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="cccf5-107">Чтобы получить ссылку на ячейку PagesX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="cccf5-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cccf5-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cccf5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cccf5-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="cccf5-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="cccf5-110">Чтобы получить ссылку на ячейку PagesX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cccf5-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cccf5-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cccf5-111">Section index:</span></span>  <br/> |<span data-ttu-id="cccf5-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cccf5-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cccf5-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cccf5-113">Row index:</span></span>  <br/> |<span data-ttu-id="cccf5-114">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="cccf5-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="cccf5-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cccf5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cccf5-116">**Виспринтпропертиеспажескс**</span><span class="sxs-lookup"><span data-stu-id="cccf5-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

