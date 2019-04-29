---
title: Ячейка X (раздел "Заметка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Представляет x-координату знака примечания в координатах страницы.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434482"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="8ba99-103">Ячейка X (раздел "Заметка")</span><span class="sxs-lookup"><span data-stu-id="8ba99-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="8ba99-104">Представляет *x*-координату знака примечания в координатах страницы.</span><span class="sxs-lookup"><span data-stu-id="8ba99-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8ba99-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="8ba99-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="8ba99-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="8ba99-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8ba99-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ba99-107">Remarks</span></span>

<span data-ttu-id="8ba99-108">Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="8ba99-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ba99-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ba99-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8ba99-110">Annotation.X[  *i*  ], где *i* = <1>, 2, 3…</span><span class="sxs-lookup"><span data-stu-id="8ba99-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8ba99-111">Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8ba99-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ba99-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8ba99-112">Section index:</span></span>  <br/> |<span data-ttu-id="8ba99-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="8ba99-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="8ba99-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8ba99-114">Row index:</span></span>  <br/> |<span data-ttu-id="8ba99-115">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="8ba99-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8ba99-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ba99-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8ba99-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="8ba99-117">**visAnnotationX**</span></span> <br/> |
   

