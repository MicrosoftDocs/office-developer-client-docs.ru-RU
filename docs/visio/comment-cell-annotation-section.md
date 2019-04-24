---
title: Comment Cell (Annotation Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Содержит текст, который отображается в комментарии.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359040"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="455b8-103">Comment Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="455b8-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="455b8-104">Содержит текст, который отображается в комментарии.</span><span class="sxs-lookup"><span data-stu-id="455b8-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="455b8-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="455b8-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="455b8-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="455b8-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="455b8-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="455b8-107">Remarks</span></span>

<span data-ttu-id="455b8-108">Чтобы получить ссылку на ячейку комментария по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="455b8-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="455b8-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="455b8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="455b8-110">Аннотация. Comment [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="455b8-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="455b8-111">Чтобы получить ссылку на ячейку Comment по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="455b8-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="455b8-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="455b8-112">Section index:</span></span>  <br/> |<span data-ttu-id="455b8-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="455b8-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="455b8-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="455b8-114">Row index:</span></span>  <br/> |<span data-ttu-id="455b8-115">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="455b8-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="455b8-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="455b8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="455b8-117">**Висаннотатионкоммент**</span><span class="sxs-lookup"><span data-stu-id="455b8-117">**visAnnotationComment**</span></span> <br/> |
   

