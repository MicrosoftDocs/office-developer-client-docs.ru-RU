---
title: Ячейка ThemeIndex (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Сохранение перечисление встроенных темы Microsoft Visio, примененная к документу, как целое число. При выборе новой темы для документа, ячейка ThemeIndex для документа и всех страниц и фигур которые он содержит обновляется индекс встроенных темы.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815013"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="3b1c5-104">Ячейка ThemeIndex (Theme Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3b1c5-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="3b1c5-105">Сохранение перечисление встроенных темы Microsoft Visio, примененная к документу, как целое число.</span><span class="sxs-lookup"><span data-stu-id="3b1c5-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="3b1c5-106">При новой темы выбран для документа ячейки **ThemeIndex** для документа и всех страниц и фигуры, которые он содержит обновляется с индексом встроенных темы.</span><span class="sxs-lookup"><span data-stu-id="3b1c5-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b1c5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b1c5-107">Remarks</span></span>

<span data-ttu-id="3b1c5-108">Для получения ссылки на ячейки **ThemeIndex** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="3b1c5-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b1c5-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3b1c5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="3b1c5-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="3b1c5-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="3b1c5-111">Для получения ссылки на ячейки **ThemeIndex** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3b1c5-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b1c5-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3b1c5-112">Section index:</span></span>  <br/> |<span data-ttu-id="3b1c5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b1c5-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b1c5-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3b1c5-114">Row index:</span></span>  <br/> |<span data-ttu-id="3b1c5-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="3b1c5-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="3b1c5-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3b1c5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="3b1c5-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="3b1c5-117">**visThemeIndex**</span></span> <br/> |
   

