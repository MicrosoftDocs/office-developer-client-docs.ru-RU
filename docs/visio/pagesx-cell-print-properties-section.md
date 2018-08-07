---
title: Ячейка PagesX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Определяет количество печатных страниц для размещения страницы документа по горизонтали.
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814350"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="51b37-103">Ячейка PagesX (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="51b37-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="51b37-104">Определяет количество печатных страниц для размещения страницы документа по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="51b37-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="51b37-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="51b37-105">Remarks</span></span>

<span data-ttu-id="51b37-106">Это значение используется только в том случае, если ячейка OnPage имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="51b37-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="51b37-107">Чтобы получить ссылку на ячейку PagesX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="51b37-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51b37-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="51b37-108">Cell name:</span></span>  <br/> | <span data-ttu-id="51b37-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="51b37-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="51b37-110">Для получения ссылки на ячейки PagesX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="51b37-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51b37-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="51b37-111">Section index:</span></span>  <br/> |<span data-ttu-id="51b37-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51b37-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51b37-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="51b37-113">Row index:</span></span>  <br/> |<span data-ttu-id="51b37-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="51b37-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="51b37-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="51b37-115">Cell index:</span></span>  <br/> |<span data-ttu-id="51b37-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="51b37-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

