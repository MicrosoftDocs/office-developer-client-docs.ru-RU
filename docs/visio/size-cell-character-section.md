---
title: Size Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Определяет размер текста в блоке текста фигуры.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314800"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="e44dc-103">Size Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="e44dc-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="e44dc-104">Определяет размер текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="e44dc-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e44dc-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e44dc-105">Remarks</span></span>

<span data-ttu-id="e44dc-106">Размер текста не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="e44dc-106">The text's size is independent of the scale of the drawing.</span></span> <span data-ttu-id="e44dc-107">Если масштаб документа изменяется, размер текста остается прежним.</span><span class="sxs-lookup"><span data-stu-id="e44dc-107">If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="e44dc-108">Чтобы получить ссылку на ячейку size по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e44dc-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e44dc-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e44dc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e44dc-110">Char. size [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e44dc-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e44dc-111">Чтобы получить ссылку на ячейку size по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e44dc-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e44dc-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e44dc-112">Section index:</span></span>  <br/> |<span data-ttu-id="e44dc-113">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="e44dc-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="e44dc-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e44dc-114">Row index:</span></span>  <br/> |<span data-ttu-id="e44dc-115">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e44dc-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e44dc-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e44dc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e44dc-117">**Висчарактерсизе**</span><span class="sxs-lookup"><span data-stu-id="e44dc-117">**visCharacterSize**</span></span> <br/> |
   

