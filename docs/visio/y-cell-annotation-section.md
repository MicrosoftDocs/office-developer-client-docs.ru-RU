---
title: Ячейка Y (раздел заметки)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Y-координата метки комментария, используемой в координаты страницы.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815202"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="5bed1-103">Ячейка Y (раздел заметки)</span><span class="sxs-lookup"><span data-stu-id="5bed1-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="5bed1-104">*Y* -координата метки комментария, используемой в координаты страницы.</span><span class="sxs-lookup"><span data-stu-id="5bed1-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bed1-105">В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd.</span><span class="sxs-lookup"><span data-stu-id="5bed1-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="5bed1-106">Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5bed1-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5bed1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bed1-107">Remarks</span></span>

<span data-ttu-id="5bed1-108">Чтобы получить ссылку на ячейку Y по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5bed1-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bed1-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5bed1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5bed1-110">Annotation.Y [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5bed1-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5bed1-111">Для получения ссылки на ячейки Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5bed1-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bed1-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5bed1-112">Section index:</span></span>  <br/> |<span data-ttu-id="5bed1-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="5bed1-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="5bed1-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5bed1-114">Row index:</span></span>  <br/> |<span data-ttu-id="5bed1-115">**visRowAnnotation** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5bed1-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5bed1-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bed1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5bed1-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="5bed1-117">**visAnnotationY**</span></span> <br/> |
   

