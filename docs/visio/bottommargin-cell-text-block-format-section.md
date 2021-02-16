---
title: BottomMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: Определяет расстояние между нижней границей текстового блока и последней строкой текста, содержащемся в нем. Значение по умолчанию — 0,1 дюйма. Это значение не зависит от масштаба рисунка. При масштабе рисования нижнее поле остается таким же.
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417212"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="24c7c-106">BottomMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="24c7c-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="24c7c-107">Определяет расстояние между нижней границей текстового блока и последней строкой текста, содержащемся в нем.</span><span class="sxs-lookup"><span data-stu-id="24c7c-107">Determines the distance between the bottom border of the text block and the last line of text it contains.</span></span> <span data-ttu-id="24c7c-108">Значение по умолчанию — 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="24c7c-108">The default is 0.1 inch.</span></span> <span data-ttu-id="24c7c-109">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="24c7c-109">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="24c7c-110">При масштабе рисования нижнее поле остается таким же.</span><span class="sxs-lookup"><span data-stu-id="24c7c-110">If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24c7c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="24c7c-111">Remarks</span></span>

<span data-ttu-id="24c7c-112">Чтобы получить ссылку на ячейку BottomMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="24c7c-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24c7c-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="24c7c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="24c7c-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="24c7c-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="24c7c-115">Чтобы получить ссылку на ячейку BottomMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="24c7c-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24c7c-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="24c7c-116">Section index:</span></span>  <br/> |<span data-ttu-id="24c7c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24c7c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="24c7c-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="24c7c-118">Row index:</span></span>  <br/> |<span data-ttu-id="24c7c-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="24c7c-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="24c7c-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="24c7c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="24c7c-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="24c7c-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

