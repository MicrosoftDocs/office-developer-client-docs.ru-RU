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
description: Указывает размер маркера.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405424"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="d755b-103">BulletSize Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="d755b-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="d755b-104">Указывает размер маркера.</span><span class="sxs-lookup"><span data-stu-id="d755b-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d755b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d755b-105">Remarks</span></span>

<span data-ttu-id="d755b-106">Это значение может быть задано для предварительно определенных или настраиваемого маркеров в виде процента или определенного значения.</span><span class="sxs-lookup"><span data-stu-id="d755b-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="d755b-107">Если значение — ноль (0), маркер имеет тот же размер шрифта, что и размер первого символа в абзаце.</span><span class="sxs-lookup"><span data-stu-id="d755b-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="d755b-108">Если значение составляет процентное значение, размер маркера составляет процент от размера шрифта первого символа в абзаце.</span><span class="sxs-lookup"><span data-stu-id="d755b-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="d755b-109">Отрицательные числа обрабатываются в процентах.</span><span class="sxs-lookup"><span data-stu-id="d755b-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="d755b-110">Чтобы получить ссылку на ячейку BulletSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d755b-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d755b-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d755b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="d755b-112">Para.BulletFontSize[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d755b-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d755b-113">Чтобы получить ссылку на ячейку BulletSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d755b-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d755b-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d755b-114">Section index:</span></span>  <br/> |<span data-ttu-id="d755b-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="d755b-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="d755b-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d755b-116">Row index:</span></span>  <br/> |<span data-ttu-id="d755b-117">**visRowParagraph**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d755b-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d755b-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d755b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d755b-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="d755b-119">**visBulletFontSize**</span></span> <br/> |
   

