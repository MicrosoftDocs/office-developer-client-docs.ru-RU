---
title: TxtPinY Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Определяет координату y центра вращения блока текста относительно начала фигуры. По умолчанию используется следующая формула:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418493"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="3addd-104">TxtPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="3addd-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="3addd-105">Определяет координату *y* центра вращения блока текста относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="3addd-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="3addd-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="3addd-106">The default formula is:</span></span> 
  
<span data-ttu-id="3addd-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="3addd-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3addd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3addd-108">Remarks</span></span>

<span data-ttu-id="3addd-109">Чтобы получить ссылку на ячейку TxtPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3addd-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3addd-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3addd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3addd-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="3addd-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="3addd-112">Чтобы получить ссылку на ячейку TxtPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3addd-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3addd-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3addd-113">Section index:</span></span>  <br/> |<span data-ttu-id="3addd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3addd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3addd-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3addd-115">Row index:</span></span>  <br/> |<span data-ttu-id="3addd-116">**Висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="3addd-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="3addd-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3addd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3addd-118">**Висксформпини**</span><span class="sxs-lookup"><span data-stu-id="3addd-118">**visXFormPinY**</span></span> <br/> |
   

