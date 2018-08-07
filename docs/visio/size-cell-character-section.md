---
title: Ячейка Size (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Определяет размер текста в блоке текста фигуры.
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814874"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="ec0d3-103">Ячейка Size (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="ec0d3-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="ec0d3-104">Определяет размер текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="ec0d3-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec0d3-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ec0d3-105">Remarks</span></span>

<span data-ttu-id="ec0d3-106">Размер текста не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="ec0d3-106">The text's size is independent of the scale of the drawing.</span></span> <span data-ttu-id="ec0d3-107">Если документа изменяется размер текста не изменится.</span><span class="sxs-lookup"><span data-stu-id="ec0d3-107">If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="ec0d3-108">Для получения ссылки на ячейки размер по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ec0d3-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec0d3-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ec0d3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ec0d3-110">Char.Size [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ec0d3-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ec0d3-111">Для получения ссылки на ячейки размер по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ec0d3-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec0d3-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ec0d3-112">Section index:</span></span>  <br/> |<span data-ttu-id="ec0d3-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ec0d3-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="ec0d3-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ec0d3-114">Row index:</span></span>  <br/> |<span data-ttu-id="ec0d3-115">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ec0d3-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ec0d3-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ec0d3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ec0d3-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="ec0d3-117">**visCharacterSize**</span></span> <br/> |
   

