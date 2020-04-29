---
title: TxtLocPinY Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Определяет координату y центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414062"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="6116e-104">TxtLocPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="6116e-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="6116e-105">Определяет координату *y* центра вращения блока текста относительно начала блока текста.</span><span class="sxs-lookup"><span data-stu-id="6116e-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="6116e-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="6116e-106">The default formula is:</span></span> 
  
<span data-ttu-id="6116e-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="6116e-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6116e-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="6116e-108">Remarks</span></span>

<span data-ttu-id="6116e-109">Чтобы получить ссылку на ячейку TxtLocPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6116e-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6116e-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6116e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6116e-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="6116e-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="6116e-112">Чтобы получить ссылку на ячейку TxtLocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6116e-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6116e-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6116e-113">Section index:</span></span>  <br/> |<span data-ttu-id="6116e-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6116e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6116e-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6116e-115">Row index:</span></span>  <br/> |<span data-ttu-id="6116e-116">**висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="6116e-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="6116e-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6116e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6116e-118">**висксформлокпини**</span><span class="sxs-lookup"><span data-stu-id="6116e-118">**visXFormLocPinY**</span></span> <br/> |
   

