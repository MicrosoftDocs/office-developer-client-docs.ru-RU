---
title: Ячейка Y (раздел "Заметка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Представляет y-координату знака примечания в координатах страницы.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360125"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="fba94-103">Ячейка Y (раздел "Заметка")</span><span class="sxs-lookup"><span data-stu-id="fba94-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="fba94-104">Представляет *y*-координату знака примечания в координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="fba94-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fba94-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="fba94-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="fba94-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="fba94-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fba94-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fba94-107">Remarks</span></span>

<span data-ttu-id="fba94-108">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="fba94-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fba94-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fba94-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fba94-110">Annotation.Y [  *i*  ], где *i* = <1>, 2, 3…</span><span class="sxs-lookup"><span data-stu-id="fba94-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fba94-111">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fba94-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fba94-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fba94-112">Section index:</span></span>  <br/> |<span data-ttu-id="fba94-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="fba94-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="fba94-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fba94-114">Row index:</span></span>  <br/> |<span data-ttu-id="fba94-115">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="fba94-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fba94-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fba94-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fba94-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="fba94-117">**visAnnotationY**</span></span> <br/> |
   

