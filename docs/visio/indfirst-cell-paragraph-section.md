---
title: Ячейка IndFirst (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Представляет расстояние от левого отступа для абзаца с отступом первой строки каждого абзаца в блоке текста фигуры. Это значение не зависит от масштаба документа. Если документа изменяется, отступ первой строки остается неизменным.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813946"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="bfcc6-105">Ячейка IndFirst (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="bfcc6-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="bfcc6-106">Представляет расстояние от левого отступа для абзаца с отступом первой строки каждого абзаца в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-106">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph.</span></span> <span data-ttu-id="bfcc6-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="bfcc6-108">Если документа изменяется, отступ первой строки остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-108">If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfcc6-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="bfcc6-109">Remarks</span></span>

<span data-ttu-id="bfcc6-110">Чтобы получить ссылку на ячейку IndFirst по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfcc6-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bfcc6-112">Para.IndFirst [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bfcc6-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bfcc6-113">Для получения ссылки на ячейки IndFirst по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfcc6-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-114">Section index:</span></span>  <br/> |<span data-ttu-id="bfcc6-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="bfcc6-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="bfcc6-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-116">Row index:</span></span>  <br/> |<span data-ttu-id="bfcc6-117">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bfcc6-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bfcc6-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bfcc6-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="bfcc6-119">**visIndentFirst**</span></span> <br/> |
   

