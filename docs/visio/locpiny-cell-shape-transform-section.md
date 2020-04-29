---
title: LocPinY Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Представляет координату центра вращения фигуры по оси y относительно начала координат фигуры. По умолчанию для определения LocPinY используется следующая формула:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410597"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="c9365-104">LocPinY Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="c9365-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="c9365-105">Представляет координату центра вращения фигуры по *оси y* относительно начала координат фигуры.</span><span class="sxs-lookup"><span data-stu-id="c9365-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="c9365-106">По умолчанию для определения LocPinY используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="c9365-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="c9365-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="c9365-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9365-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9365-108">Remarks</span></span>

<span data-ttu-id="c9365-109">Чтобы получить ссылку на ячейку LocPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c9365-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9365-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c9365-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c9365-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="c9365-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="c9365-112">Чтобы получить ссылку на ячейку LocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c9365-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9365-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c9365-113">Section index:</span></span>  <br/> |<span data-ttu-id="c9365-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9365-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c9365-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c9365-115">Row index:</span></span>  <br/> |<span data-ttu-id="c9365-116">**висровксформаут**</span><span class="sxs-lookup"><span data-stu-id="c9365-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="c9365-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c9365-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c9365-118">**висксформлокпини**</span><span class="sxs-lookup"><span data-stu-id="c9365-118">**visXFormLocPinY**</span></span> <br/> |
   

