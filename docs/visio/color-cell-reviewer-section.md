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
description: Значение RGB, которое представляет цвет, присвоенный разметке рецензента документов.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430541"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="5b732-103">Color Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="5b732-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="5b732-104">Значение RGB, которое представляет цвет, присвоенный разметке рецензента документов.</span><span class="sxs-lookup"><span data-stu-id="5b732-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b732-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b732-105">Remarks</span></span>

<span data-ttu-id="5b732-106">Цвета назначены рецензентам в следующей последовательности: красный, синий, зеленый, фиолетовый, оранжевый, бирюзовый, серый.</span><span class="sxs-lookup"><span data-stu-id="5b732-106">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray.</span></span> <span data-ttu-id="5b732-107">Эти цвета снова циклика для остальных рецензентов.</span><span class="sxs-lookup"><span data-stu-id="5b732-107">These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="5b732-108">Комментарии, вступив на исходной странице рисования, всегда окрашены в желтый цвет независимо от цвета, назначенного рецензенту в ячейке Color.</span><span class="sxs-lookup"><span data-stu-id="5b732-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="5b732-109">Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5b732-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b732-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5b732-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5b732-111">Reviewer.Color  *[i]*  где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5b732-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5b732-112">Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5b732-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b732-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5b732-113">Section index:</span></span>  <br/> |<span data-ttu-id="5b732-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="5b732-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="5b732-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5b732-115">Row index:</span></span>  <br/> |<span data-ttu-id="5b732-116">**visRowReviewer**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="5b732-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5b732-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5b732-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5b732-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="5b732-118">**visReviewerColor**</span></span> <br/> |
   

