---
title: Ячейка Date (раздел "Примечание")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Содержит дату и время последнего изменения комментария.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813558"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="801cb-103">Ячейка Date (раздел "Примечание")</span><span class="sxs-lookup"><span data-stu-id="801cb-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="801cb-104">Содержит дату и время последнего изменения комментария.</span><span class="sxs-lookup"><span data-stu-id="801cb-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="801cb-105">В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd.</span><span class="sxs-lookup"><span data-stu-id="801cb-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="801cb-106">Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="801cb-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="801cb-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="801cb-107">Remarks</span></span>

<span data-ttu-id="801cb-108">В поле комментария в пользовательском интерфейсе отображается только дата.</span><span class="sxs-lookup"><span data-stu-id="801cb-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="801cb-109">Для получения ссылки на ячейки даты по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="801cb-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="801cb-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="801cb-110">Cell name:</span></span>  <br/> | <span data-ttu-id="801cb-111">Annotation.Date [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="801cb-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="801cb-112">Для получения ссылки на ячейки даты по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="801cb-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="801cb-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="801cb-113">Section index:</span></span>  <br/> |<span data-ttu-id="801cb-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="801cb-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="801cb-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="801cb-115">Row index:</span></span>  <br/> |<span data-ttu-id="801cb-116">**visRowAnnotation** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="801cb-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="801cb-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="801cb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="801cb-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="801cb-118">**visAnnotationDate**</span></span> <br/> |
   

