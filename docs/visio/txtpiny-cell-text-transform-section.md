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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316424"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="e8dbc-104">TxtPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="e8dbc-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="e8dbc-105">Определяет координату *y* центра вращения блока текста относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="e8dbc-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-106">The default formula is:</span></span> 
  
<span data-ttu-id="e8dbc-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="e8dbc-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8dbc-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8dbc-108">Remarks</span></span>

<span data-ttu-id="e8dbc-109">Чтобы получить ссылку на ячейку TxtPinY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dbc-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e8dbc-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="e8dbc-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="e8dbc-112">Чтобы получить ссылку на ячейку TxtPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8dbc-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-113">Section index:</span></span>  <br/> |<span data-ttu-id="e8dbc-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8dbc-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8dbc-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-115">Row index:</span></span>  <br/> |<span data-ttu-id="e8dbc-116">**Висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="e8dbc-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e8dbc-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8dbc-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e8dbc-118">**Висксформпини**</span><span class="sxs-lookup"><span data-stu-id="e8dbc-118">**visXFormPinY**</span></span> <br/> |
   

