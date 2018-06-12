---
title: Положение ячейки (вкладки раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Задает позиции табуляции. Положение вкладки не зависит от масштаба документа. Если документа изменяется, положение вкладки не изменится.
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814481"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="bb782-105">Положение ячейки (вкладки раздел)</span><span class="sxs-lookup"><span data-stu-id="bb782-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="bb782-106">Задает позиции табуляции.</span><span class="sxs-lookup"><span data-stu-id="bb782-106">Specifies the position of a tab stop.</span></span> <span data-ttu-id="bb782-107">Положение вкладки не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="bb782-107">The tab position is independent of the scale of the drawing.</span></span> <span data-ttu-id="bb782-108">Если документа изменяется, положение вкладки не изменится.</span><span class="sxs-lookup"><span data-stu-id="bb782-108">If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb782-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="bb782-109">Remarks</span></span>

<span data-ttu-id="bb782-110">Для получения ссылки на ячейки положение по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bb782-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb782-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bb782-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bb782-112">Вкладки.</span><span class="sxs-lookup"><span data-stu-id="bb782-112">Tabs.</span></span>  <span data-ttu-id="bb782-113">*ij* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bb782-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bb782-114">Для получения ссылки на ячейки положение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bb782-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb782-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bb782-115">Section index:</span></span>  <br/> |<span data-ttu-id="bb782-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="bb782-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="bb782-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bb782-117">Row index:</span></span>  <br/> |<span data-ttu-id="bb782-118">**visRowTab** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bb782-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bb782-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bb782-119">Cell index:</span></span>  <br/> | <span data-ttu-id="bb782-120">(*j* \* 3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="bb782-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

