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
description: Определяет размер текста в текстовом блоке фигуры.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415602"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="2e08e-103">Size Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="2e08e-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="2e08e-104">Определяет размер текста в текстовом блоке фигуры.</span><span class="sxs-lookup"><span data-stu-id="2e08e-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e08e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e08e-105">Remarks</span></span>

<span data-ttu-id="2e08e-106">Размер текста не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="2e08e-106">The text's size is independent of the scale of the drawing.</span></span> <span data-ttu-id="2e08e-107">Если документ масштабировать, размер текста остается тем же.</span><span class="sxs-lookup"><span data-stu-id="2e08e-107">If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="2e08e-108">Чтобы получить ссылку на ячейку Size по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2e08e-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e08e-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e08e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2e08e-110">Char.Size[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2e08e-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2e08e-111">Чтобы получить ссылку на ячейку Size по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2e08e-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e08e-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2e08e-112">Section index:</span></span>  <br/> |<span data-ttu-id="2e08e-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2e08e-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="2e08e-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2e08e-114">Row index:</span></span>  <br/> |<span data-ttu-id="2e08e-115">**visRowCharacter**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2e08e-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2e08e-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e08e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2e08e-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="2e08e-117">**visCharacterSize**</span></span> <br/> |
   

