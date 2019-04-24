---
title: Position Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Указывает позицию табуляции. Позиция табуляции не зависит от масштаба документа. Если масштаб документа изменяется, положение вкладки остается прежним.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307751"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="d6d71-105">Position Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="d6d71-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="d6d71-106">Указывает позицию табуляции.</span><span class="sxs-lookup"><span data-stu-id="d6d71-106">Specifies the position of a tab stop.</span></span> <span data-ttu-id="d6d71-107">Позиция табуляции не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="d6d71-107">The tab position is independent of the scale of the drawing.</span></span> <span data-ttu-id="d6d71-108">Если масштаб документа изменяется, положение вкладки остается прежним.</span><span class="sxs-lookup"><span data-stu-id="d6d71-108">If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6d71-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6d71-109">Remarks</span></span>

<span data-ttu-id="d6d71-110">Чтобы получить ссылку на ячейку Position по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d6d71-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6d71-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d6d71-111">Cell name:</span></span>  <br/> | <span data-ttu-id="d6d71-112">Знаков.</span><span class="sxs-lookup"><span data-stu-id="d6d71-112">Tabs.</span></span>  <span data-ttu-id="d6d71-113">*ИЖ* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d6d71-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d6d71-114">Чтобы получить ссылку на ячейку Position по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d6d71-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6d71-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d6d71-115">Section index:</span></span>  <br/> |<span data-ttu-id="d6d71-116">**Виссектионтаб**</span><span class="sxs-lookup"><span data-stu-id="d6d71-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="d6d71-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d6d71-117">Row index:</span></span>  <br/> |<span data-ttu-id="d6d71-118">**висровтаб** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d6d71-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d6d71-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d6d71-119">Cell index:</span></span>  <br/> | <span data-ttu-id="d6d71-120">(*j* \* 3) + **вистабпос**</span><span class="sxs-lookup"><span data-stu-id="d6d71-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

