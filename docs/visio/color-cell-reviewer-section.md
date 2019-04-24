---
title: Color Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Значение RGB, представляющее цвет, назначенный разметке рецензента документов.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341820"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="93478-103">Color Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="93478-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="93478-104">Значение RGB, представляющее цвет, назначенный разметке рецензента документов.</span><span class="sxs-lookup"><span data-stu-id="93478-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="93478-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93478-105">Remarks</span></span>

<span data-ttu-id="93478-106">Цвета назначаются проверяющим в следующей последовательности: Red, Blue, Green, фиолетовый, оранжевый, бирюзовый, серый.</span><span class="sxs-lookup"><span data-stu-id="93478-106">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray.</span></span> <span data-ttu-id="93478-107">Эти цвета циклически передаются для всех оставшихся рецензентов.</span><span class="sxs-lookup"><span data-stu-id="93478-107">These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="93478-108">Комментарии, введенные на исходной странице документа, всегда окрашены желтым цветом, независимо от цвета, назначенного рецензенту в ячейке Color (цвет).</span><span class="sxs-lookup"><span data-stu-id="93478-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="93478-109">Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="93478-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93478-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="93478-110">Cell name:</span></span>  <br/> | <span data-ttu-id="93478-111">Review. Color [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="93478-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="93478-112">Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="93478-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93478-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93478-113">Section index:</span></span>  <br/> |<span data-ttu-id="93478-114">**Виссектионревиевер**</span><span class="sxs-lookup"><span data-stu-id="93478-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="93478-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93478-115">Row index:</span></span>  <br/> |<span data-ttu-id="93478-116">**висровревиевер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="93478-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="93478-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93478-117">Cell index:</span></span>  <br/> |<span data-ttu-id="93478-118">**Висревиеверколор**</span><span class="sxs-lookup"><span data-stu-id="93478-118">**visReviewerColor**</span></span> <br/> |
   

