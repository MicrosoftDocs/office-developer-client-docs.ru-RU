---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Сохраняет в качестве встроенной темы microsoft Visio, применяемой к документу, в качестве встроенной. Когда для документа выбрана новая тема, ячейка ThemeIndex для документа, а также все страницы и фигуры, которые в нем содержатся, обновляется с помощью индекса встроенной темы.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411913"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="81dd7-104">ThemeIndex Cell (Theme Properties Section)</span><span class="sxs-lookup"><span data-stu-id="81dd7-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="81dd7-105">Сохраняет в качестве встроенной темы microsoft Visio, применяемой к документу, в качестве встроенной.</span><span class="sxs-lookup"><span data-stu-id="81dd7-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="81dd7-106">Когда для документа выбрана новая тема, ячейка **ThemeIndex** для документа, а также все страницы и фигуры, которые в нем содержатся, обновляется с помощью индекса встроенной темы.</span><span class="sxs-lookup"><span data-stu-id="81dd7-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81dd7-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="81dd7-107">Remarks</span></span>

<span data-ttu-id="81dd7-108">Чтобы получить ссылку на ячейку **ThemeIndex** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="81dd7-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81dd7-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="81dd7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="81dd7-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="81dd7-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="81dd7-111">Чтобы получить ссылку на **ячейку ThemeIndex** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="81dd7-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81dd7-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81dd7-112">Section index:</span></span>  <br/> |<span data-ttu-id="81dd7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81dd7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81dd7-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81dd7-114">Row index:</span></span>  <br/> |<span data-ttu-id="81dd7-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="81dd7-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="81dd7-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81dd7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="81dd7-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="81dd7-117">**visThemeIndex**</span></span> <br/> |
   

