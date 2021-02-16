---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Определяет цвет шрифта из быстрых стилей, наследуемый текстом фигуры от активной темы, в виде integer от 0 до 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415028"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="145a1-103">QuickStyleFontColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="145a1-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="145a1-104">Определяет цвет шрифта из быстрых стилей, наследуемый текстом фигуры от активной темы, в виде integer от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="145a1-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="145a1-105">Значение</span><span class="sxs-lookup"><span data-stu-id="145a1-105">Value</span></span>  <br/> |<span data-ttu-id="145a1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="145a1-106">Description</span></span>  <br/> |
|<span data-ttu-id="145a1-107">0</span><span class="sxs-lookup"><span data-stu-id="145a1-107">0</span></span>  <br/> |<span data-ttu-id="145a1-108">Текст фигуры использует цвет темного шрифта.</span><span class="sxs-lookup"><span data-stu-id="145a1-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="145a1-109">1 </span><span class="sxs-lookup"><span data-stu-id="145a1-109">1</span></span>  <br/> |<span data-ttu-id="145a1-110">Текст фигуры использует цвет шрифта Light.</span><span class="sxs-lookup"><span data-stu-id="145a1-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="145a1-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="145a1-111">Remarks</span></span>

<span data-ttu-id="145a1-112">Чтобы получить ссылку на ячейку **QuickStyleFontColor** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="145a1-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="145a1-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="145a1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="145a1-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="145a1-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="145a1-115">Чтобы получить ссылку на ячейку **QuickStyleFontColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="145a1-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="145a1-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="145a1-116">Section index:</span></span>  <br/> |<span data-ttu-id="145a1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="145a1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="145a1-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="145a1-118">Row index:</span></span>  <br/> |<span data-ttu-id="145a1-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="145a1-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="145a1-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="145a1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="145a1-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="145a1-121">**visQuickStyleFontColor**</span></span> <br/> |
   

