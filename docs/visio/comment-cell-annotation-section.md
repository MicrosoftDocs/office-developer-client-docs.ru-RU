---
title: Ячейка Comment (раздел "Примечание")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Содержит текст, который отображается в комментарий.
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813405"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="5ca6f-103">Ячейка Comment (раздел "Примечание")</span><span class="sxs-lookup"><span data-stu-id="5ca6f-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="5ca6f-104">Содержит текст, который отображается в комментарий.</span><span class="sxs-lookup"><span data-stu-id="5ca6f-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5ca6f-105">В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd.</span><span class="sxs-lookup"><span data-stu-id="5ca6f-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="5ca6f-106">Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5ca6f-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5ca6f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ca6f-107">Remarks</span></span>

<span data-ttu-id="5ca6f-108">Чтобы получить ссылку на ячейку комментария по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5ca6f-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ca6f-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5ca6f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5ca6f-110">Annotation.Comment [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5ca6f-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ca6f-111">Для получения ссылки на ячейки комментарий по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5ca6f-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ca6f-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5ca6f-112">Section index:</span></span>  <br/> |<span data-ttu-id="5ca6f-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="5ca6f-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="5ca6f-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5ca6f-114">Row index:</span></span>  <br/> |<span data-ttu-id="5ca6f-115">**visRowAnnotation** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ca6f-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ca6f-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5ca6f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5ca6f-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="5ca6f-117">**visAnnotationComment**</span></span> <br/> |
   

