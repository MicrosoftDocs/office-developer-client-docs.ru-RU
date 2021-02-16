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
description: 'Определяет координату Y центра вращения текстового блока относительно начала фигуры. Формула по умолчанию:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418493"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="20c4b-104">TxtPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="20c4b-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="20c4b-105">Определяет  *координату Y*  центра вращения текстового блока относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="20c4b-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="20c4b-106">Формула по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="20c4b-106">The default formula is:</span></span> 
  
<span data-ttu-id="20c4b-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="20c4b-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20c4b-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="20c4b-108">Remarks</span></span>

<span data-ttu-id="20c4b-109">Чтобы получить ссылку на ячейку TxtPinY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="20c4b-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20c4b-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="20c4b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="20c4b-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="20c4b-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="20c4b-112">Чтобы получить ссылку на ячейку TxtPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="20c4b-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20c4b-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="20c4b-113">Section index:</span></span>  <br/> |<span data-ttu-id="20c4b-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20c4b-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20c4b-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="20c4b-115">Row index:</span></span>  <br/> |<span data-ttu-id="20c4b-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="20c4b-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="20c4b-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="20c4b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="20c4b-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="20c4b-118">**visXFormPinY**</span></span> <br/> |
   

