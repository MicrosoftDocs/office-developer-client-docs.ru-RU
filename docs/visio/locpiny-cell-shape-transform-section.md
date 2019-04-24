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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358046"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="3f001-104">LocPinY Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="3f001-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="3f001-105">Представляет координату центра вращения фигуры по *оси y* относительно начала координат фигуры.</span><span class="sxs-lookup"><span data-stu-id="3f001-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="3f001-106">По умолчанию для определения LocPinY используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="3f001-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="3f001-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="3f001-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f001-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f001-108">Remarks</span></span>

<span data-ttu-id="3f001-109">Чтобы получить ссылку на ячейку LocPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3f001-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f001-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3f001-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3f001-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="3f001-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="3f001-112">Чтобы получить ссылку на ячейку LocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3f001-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f001-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3f001-113">Section index:</span></span>  <br/> |<span data-ttu-id="3f001-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f001-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f001-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3f001-115">Row index:</span></span>  <br/> |<span data-ttu-id="3f001-116">**Висровксформаут**</span><span class="sxs-lookup"><span data-stu-id="3f001-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="3f001-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3f001-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3f001-118">**Висксформлокпини**</span><span class="sxs-lookup"><span data-stu-id="3f001-118">**visXFormLocPinY**</span></span> <br/> |
   

