---
title: TxtWidth Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Определяет ширину блока текста. По умолчанию используется следующая формула:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426095"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="fe7b8-104">TxtWidth Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="fe7b8-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="fe7b8-105">Определяет ширину блока текста.</span><span class="sxs-lookup"><span data-stu-id="fe7b8-105">Determines the width of the text block.</span></span> <span data-ttu-id="fe7b8-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-106">The default formula is:</span></span>
  
<span data-ttu-id="fe7b8-107">= Width \* 1</span><span class="sxs-lookup"><span data-stu-id="fe7b8-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe7b8-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe7b8-108">Remarks</span></span>

<span data-ttu-id="fe7b8-109">Чтобы получить ссылку на ячейку TxtWidth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe7b8-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fe7b8-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="fe7b8-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="fe7b8-112">Чтобы получить ссылку на ячейку TxtWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe7b8-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-113">Section index:</span></span>  <br/> |<span data-ttu-id="fe7b8-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fe7b8-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-115">Row index:</span></span>  <br/> |<span data-ttu-id="fe7b8-116">**Висровтекстксформ**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="fe7b8-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe7b8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fe7b8-118">**Висксформвидс**</span><span class="sxs-lookup"><span data-stu-id="fe7b8-118">**visXFormWidth**</span></span> <br/> |
   

