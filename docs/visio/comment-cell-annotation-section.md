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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415532"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="fe2ab-103">Comment Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="fe2ab-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="fe2ab-104">Содержит текст, который отображается в комментарии.</span><span class="sxs-lookup"><span data-stu-id="fe2ab-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe2ab-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="fe2ab-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="fe2ab-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="fe2ab-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe2ab-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe2ab-107">Remarks</span></span>

<span data-ttu-id="fe2ab-108">Чтобы получить ссылку на ячейку Comment по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe2ab-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fe2ab-110">Аннотация.Comment[i] где *i* = <1>, 2, 3 ... </span><span class="sxs-lookup"><span data-stu-id="fe2ab-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fe2ab-111">Чтобы получить ссылку на ячейку Comment по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe2ab-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-112">Section index:</span></span>  <br/> |<span data-ttu-id="fe2ab-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="fe2ab-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="fe2ab-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-114">Row index:</span></span>  <br/> |<span data-ttu-id="fe2ab-115">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="fe2ab-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fe2ab-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe2ab-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fe2ab-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="fe2ab-117">**visAnnotationComment**</span></span> <br/> |
   

