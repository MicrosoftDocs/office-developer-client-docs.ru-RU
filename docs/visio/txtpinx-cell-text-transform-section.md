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
description: 'Определяет x-координату центра вращения текстового блока по отношению к происхождению фигуры. Формула по умолчанию:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423498"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="c7248-104">TxtPinX Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="c7248-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="c7248-105">Определяет  *x-координату*  центра вращения текстового блока по отношению к происхождению фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7248-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="c7248-106">Формула по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c7248-106">The default formula is:</span></span> 
  
<span data-ttu-id="c7248-107">= \* Ширина 0,5</span><span class="sxs-lookup"><span data-stu-id="c7248-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7248-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7248-108">Remarks</span></span>

<span data-ttu-id="c7248-109">Чтобы получить ссылку на ячейку TxtPinX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c7248-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7248-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c7248-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c7248-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="c7248-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="c7248-112">Чтобы получить ссылку на ячейку TxtPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c7248-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7248-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c7248-113">Section index:</span></span>  <br/> |<span data-ttu-id="c7248-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7248-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7248-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c7248-115">Row index:</span></span>  <br/> |<span data-ttu-id="c7248-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="c7248-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="c7248-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c7248-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c7248-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="c7248-118">**visXFormPinX**</span></span> <br/> |
   

