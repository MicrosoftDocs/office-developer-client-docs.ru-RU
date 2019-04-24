---
title: TxtPinX Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Определяет координату x центра вращения блока текста относительно начала фигуры. По умолчанию используется следующая формула:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282301"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="2dcc5-104">TxtPinX Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="2dcc5-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="2dcc5-105">Определяет координату *x* центра вращения блока текста относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="2dcc5-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="2dcc5-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-106">The default formula is:</span></span> 
  
<span data-ttu-id="2dcc5-107">= Ширина \* 0,5</span><span class="sxs-lookup"><span data-stu-id="2dcc5-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dcc5-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2dcc5-108">Remarks</span></span>

<span data-ttu-id="2dcc5-109">Чтобы получить ссылку на ячейку TxtPinX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2dcc5-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2dcc5-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="2dcc5-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="2dcc5-112">Чтобы получить ссылку на ячейку TxtPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2dcc5-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-113">Section index:</span></span>  <br/> |<span data-ttu-id="2dcc5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2dcc5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2dcc5-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-115">Row index:</span></span>  <br/> |<span data-ttu-id="2dcc5-116">**Висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="2dcc5-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="2dcc5-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2dcc5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2dcc5-118">**Висксформпинкс**</span><span class="sxs-lookup"><span data-stu-id="2dcc5-118">**visXFormPinX**</span></span> <br/> |
   

