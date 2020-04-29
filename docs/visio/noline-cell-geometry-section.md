---
title: NoLine Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Определяет, отображается ли линия вокруг границы пути.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433754"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="e96f9-103">NoLine Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e96f9-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="e96f9-104">Определяет, отображается ли линия вокруг границы пути.</span><span class="sxs-lookup"><span data-stu-id="e96f9-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="e96f9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e96f9-105">**Value**</span></span>|<span data-ttu-id="e96f9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e96f9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e96f9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e96f9-107">TRUE</span></span>  <br/> | <span data-ttu-id="e96f9-108">Линия не рисуется вокруг границы контура, который является границей области заливки.</span><span class="sxs-lookup"><span data-stu-id="e96f9-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="e96f9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e96f9-109">FALSE</span></span>  <br/> | <span data-ttu-id="e96f9-110">Линия рисуется вокруг границы пути.</span><span class="sxs-lookup"><span data-stu-id="e96f9-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e96f9-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e96f9-111">Remarks</span></span>

<span data-ttu-id="e96f9-112">Когда вы меняете цвет линии на белый, линия остается в наличии, даже если она не видна на белом фоне.</span><span class="sxs-lookup"><span data-stu-id="e96f9-112">When you change the color of a line to white, the line still exists even though you can't see it on a white background.</span></span> <span data-ttu-id="e96f9-113">Если ячейке присвоено значение TRUE, никакая строка не отображается.</span><span class="sxs-lookup"><span data-stu-id="e96f9-113">When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="e96f9-114">Чтобы получить ссылку на ячейку "inline" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="e96f9-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e96f9-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e96f9-115">Cell name:</span></span>  <br/> | <span data-ttu-id="e96f9-116">Геометрия *i* . Inline, где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e96f9-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e96f9-117">Чтобы получить ссылку на ячейку Inline по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e96f9-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e96f9-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e96f9-118">Section index:</span></span>  <br/> |<span data-ttu-id="e96f9-119">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e96f9-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e96f9-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e96f9-120">Row index:</span></span>  <br/> |<span data-ttu-id="e96f9-121">**висровкомпонент**</span><span class="sxs-lookup"><span data-stu-id="e96f9-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="e96f9-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e96f9-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e96f9-123">**вискомпнолине**</span><span class="sxs-lookup"><span data-stu-id="e96f9-123">**visCompNoLine**</span></span> <br/> |
   

