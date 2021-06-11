---
title: Date Cell (Annotation Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Содержит дату и время последнего редактирования комментария.
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423883"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="737c9-103">Date Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="737c9-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="737c9-104">Содержит дату и время последнего редактирования комментария.</span><span class="sxs-lookup"><span data-stu-id="737c9-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="737c9-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="737c9-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="737c9-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="737c9-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="737c9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="737c9-107">Remarks</span></span>

<span data-ttu-id="737c9-108">Только дата отображается в поле комментариев в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="737c9-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="737c9-109">Чтобы получить ссылку на ячейку Date по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="737c9-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="737c9-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="737c9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="737c9-111">Аннотация.Date[i] где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="737c9-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="737c9-112">Чтобы получить ссылку на ячейку Date по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="737c9-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="737c9-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="737c9-113">Section index:</span></span>  <br/> |<span data-ttu-id="737c9-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="737c9-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="737c9-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="737c9-115">Row index:</span></span>  <br/> |<span data-ttu-id="737c9-116">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="737c9-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="737c9-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="737c9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="737c9-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="737c9-118">**visAnnotationDate**</span></span> <br/> |
   

