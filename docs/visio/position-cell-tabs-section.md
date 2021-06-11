---
title: Position Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Указывает положение остановки вкладки. Положение вкладки не зависит от масштаба рисунка. Если рисунок масштабировать, положение вкладки остается таким же.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409932"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="a2755-105">Position Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="a2755-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="a2755-106">Указывает положение остановки вкладки.</span><span class="sxs-lookup"><span data-stu-id="a2755-106">Specifies the position of a tab stop.</span></span> <span data-ttu-id="a2755-107">Положение вкладки не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="a2755-107">The tab position is independent of the scale of the drawing.</span></span> <span data-ttu-id="a2755-108">Если рисунок масштабировать, положение вкладки остается таким же.</span><span class="sxs-lookup"><span data-stu-id="a2755-108">If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2755-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2755-109">Remarks</span></span>

<span data-ttu-id="a2755-110">Чтобы получить ссылку на ячейку Position по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a2755-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2755-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a2755-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a2755-112">Вкладки.</span><span class="sxs-lookup"><span data-stu-id="a2755-112">Tabs.</span></span>  <span data-ttu-id="a2755-113">*ij,*            *где i*  и  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a2755-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a2755-114">Чтобы получить ссылку на ячейку Position по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a2755-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2755-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a2755-115">Section index:</span></span>  <br/> |<span data-ttu-id="a2755-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="a2755-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="a2755-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a2755-117">Row index:</span></span>  <br/> |<span data-ttu-id="a2755-118">**visRowTab**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="a2755-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a2755-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a2755-119">Cell index:</span></span>  <br/> | <span data-ttu-id="a2755-120">(*j*  \*3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="a2755-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

