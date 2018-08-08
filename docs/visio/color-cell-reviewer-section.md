---
title: Ячейка Color (раздел "Рецензент")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Значение RGB, представляющее цвет, назначенный разметки рецензент документа.
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813407"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="06aaf-103">Ячейка Color (раздел "Рецензент")</span><span class="sxs-lookup"><span data-stu-id="06aaf-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="06aaf-104">Значение RGB, представляющее цвет, назначенный разметки рецензент документа.</span><span class="sxs-lookup"><span data-stu-id="06aaf-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="06aaf-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="06aaf-105">Remarks</span></span>

<span data-ttu-id="06aaf-106">Цвета назначаются рецензентов в следующей последовательности: красный, синий, зеленый, фиолетовые, оранжевый, turquoise, серый.</span><span class="sxs-lookup"><span data-stu-id="06aaf-106">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray.</span></span> <span data-ttu-id="06aaf-107">Эти цвета переключения еще раз для любого остальных рецензентов.</span><span class="sxs-lookup"><span data-stu-id="06aaf-107">These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="06aaf-108">Комментарии, введенные на странице исходного документа всегда желтый цвет, независимо от того, цвет, назначенный проверяющему в ячейке цвет.</span><span class="sxs-lookup"><span data-stu-id="06aaf-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="06aaf-109">Для получения ссылки на ячейки цвет по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="06aaf-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06aaf-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="06aaf-110">Cell name:</span></span>  <br/> | <span data-ttu-id="06aaf-111">Reviewer.Color [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="06aaf-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="06aaf-112">Для получения ссылки на ячейки цвет по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="06aaf-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06aaf-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="06aaf-113">Section index:</span></span>  <br/> |<span data-ttu-id="06aaf-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="06aaf-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="06aaf-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="06aaf-115">Row index:</span></span>  <br/> |<span data-ttu-id="06aaf-116">**visRowReviewer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="06aaf-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="06aaf-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="06aaf-117">Cell index:</span></span>  <br/> |<span data-ttu-id="06aaf-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="06aaf-118">**visReviewerColor**</span></span> <br/> |
   

