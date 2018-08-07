---
title: Ячейка PagesY (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Определяет количество печатных страниц для размещения страницы документа по вертикали.
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814343"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="043fd-103">Ячейка PagesY (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="043fd-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="043fd-104">Определяет количество печатных страниц для размещения страницы документа по вертикали.</span><span class="sxs-lookup"><span data-stu-id="043fd-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="043fd-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="043fd-105">Remarks</span></span>

<span data-ttu-id="043fd-106">Это значение используется только в том случае, если ячейка OnPage имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="043fd-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="043fd-107">Чтобы получить ссылку на ячейку PagesY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="043fd-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="043fd-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="043fd-108">Cell name:</span></span>  <br/> | <span data-ttu-id="043fd-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="043fd-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="043fd-110">Для получения ссылки на ячейки PagesY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="043fd-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="043fd-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="043fd-111">Section index:</span></span>  <br/> |<span data-ttu-id="043fd-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="043fd-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="043fd-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="043fd-113">Row index:</span></span>  <br/> |<span data-ttu-id="043fd-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="043fd-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="043fd-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="043fd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="043fd-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="043fd-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

