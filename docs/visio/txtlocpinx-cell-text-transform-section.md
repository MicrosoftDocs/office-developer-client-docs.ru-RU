---
title: TxtLocPinX Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Определяет координату x центра вращения блока текста относительно начала блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425857"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="85fc0-104">TxtLocPinX Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="85fc0-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="85fc0-105">Определяет координату *x* центра вращения блока текста относительно начала блока текста.</span><span class="sxs-lookup"><span data-stu-id="85fc0-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="85fc0-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="85fc0-106">The default formula is:</span></span> 
  
<span data-ttu-id="85fc0-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="85fc0-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="85fc0-108">Эта формула вычисляется как горизонтальный центр блока текста.</span><span class="sxs-lookup"><span data-stu-id="85fc0-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85fc0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="85fc0-109">Remarks</span></span>

<span data-ttu-id="85fc0-110">Чтобы получить ссылку на ячейку TxtLocPinX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="85fc0-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85fc0-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="85fc0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="85fc0-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="85fc0-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="85fc0-113">Чтобы получить ссылку на ячейку TxtLocPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="85fc0-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85fc0-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="85fc0-114">Section index:</span></span>  <br/> |<span data-ttu-id="85fc0-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85fc0-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="85fc0-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="85fc0-116">Row index:</span></span>  <br/> |<span data-ttu-id="85fc0-117">**висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="85fc0-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="85fc0-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="85fc0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="85fc0-119">**висксформлокпинкс**</span><span class="sxs-lookup"><span data-stu-id="85fc0-119">**visXFormLocPinX**</span></span> <br/> |
   

