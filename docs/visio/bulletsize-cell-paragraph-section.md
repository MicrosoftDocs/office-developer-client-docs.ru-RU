---
title: BulletSize Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Задает размер маркера.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337613"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="55a1b-103">BulletSize Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="55a1b-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="55a1b-104">Задает размер маркера.</span><span class="sxs-lookup"><span data-stu-id="55a1b-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55a1b-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55a1b-105">Remarks</span></span>

<span data-ttu-id="55a1b-106">Это значение может быть указано для стандартных или настраиваемых маркеров в виде процента или определенного значения.</span><span class="sxs-lookup"><span data-stu-id="55a1b-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="55a1b-107">Если значение равно нулю (0), маркер будет иметь тот же размер шрифта, что и первый знак абзаца.</span><span class="sxs-lookup"><span data-stu-id="55a1b-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="55a1b-108">Если значение равно проценту, то размер маркера будет изменяться в процентах от размера шрифта первого символа абзаца.</span><span class="sxs-lookup"><span data-stu-id="55a1b-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="55a1b-109">Отрицательные числа обрабатываются как проценты.</span><span class="sxs-lookup"><span data-stu-id="55a1b-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="55a1b-110">Чтобы получить ссылку на ячейку BulletSize по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="55a1b-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55a1b-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="55a1b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="55a1b-112">Para. Буллетфонтсизе [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="55a1b-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="55a1b-113">Чтобы получить ссылку на ячейку BulletSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="55a1b-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55a1b-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="55a1b-114">Section index:</span></span>  <br/> |<span data-ttu-id="55a1b-115">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="55a1b-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="55a1b-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="55a1b-116">Row index:</span></span>  <br/> |<span data-ttu-id="55a1b-117">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="55a1b-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="55a1b-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="55a1b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="55a1b-119">**Висбуллетфонтсизе**</span><span class="sxs-lookup"><span data-stu-id="55a1b-119">**visBulletFontSize**</span></span> <br/> |
   

