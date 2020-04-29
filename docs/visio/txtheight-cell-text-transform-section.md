---
title: TxtHeight Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Определяет высоту блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409309"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="dd857-104">TxtHeight Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="dd857-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="dd857-105">Определяет высоту блока текста.</span><span class="sxs-lookup"><span data-stu-id="dd857-105">Determines the height of the text block.</span></span> <span data-ttu-id="dd857-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="dd857-106">The default formula is:</span></span>
  
<span data-ttu-id="dd857-107">= Высота \* 1</span><span class="sxs-lookup"><span data-stu-id="dd857-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd857-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="dd857-108">Remarks</span></span>

<span data-ttu-id="dd857-109">Чтобы получить ссылку на ячейку TxtHeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dd857-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd857-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd857-110">Cell name:</span></span>  <br/> | <span data-ttu-id="dd857-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="dd857-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="dd857-112">Чтобы получить ссылку на ячейку TxtHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dd857-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd857-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dd857-113">Section index:</span></span>  <br/> |<span data-ttu-id="dd857-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd857-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dd857-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dd857-115">Row index:</span></span>  <br/> |<span data-ttu-id="dd857-116">**висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="dd857-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="dd857-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd857-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dd857-118">**висксформхеигхт**</span><span class="sxs-lookup"><span data-stu-id="dd857-118">**visXFormHeight**</span></span> <br/> |
   

