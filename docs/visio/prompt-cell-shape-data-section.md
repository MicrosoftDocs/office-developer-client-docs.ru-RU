---
title: Prompt Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Указывает описательный или инструктивный текст, который отображается как подсказка при приостановке мыши над значением в окне "Данные фигуры".
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405487"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="f5271-103">Prompt Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="f5271-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="f5271-104">Указывает описательный или инструктивный текст, который отображается как подсказка при приостановке мыши над значением в окне **"Данные** фигуры".</span><span class="sxs-lookup"><span data-stu-id="f5271-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5271-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f5271-105">Remarks</span></span>

<span data-ttu-id="f5271-106">Чтобы получить ссылку на ячейку Prompt по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f5271-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5271-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f5271-107">Cell name:</span></span>  <br/> | <span data-ttu-id="f5271-108">Реквизит.  *Имя*  . Запрос,  *где Name*  — имя строки</span><span class="sxs-lookup"><span data-stu-id="f5271-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f5271-109">Чтобы получить ссылку на ячейку Prompt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f5271-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5271-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f5271-110">Section index:</span></span>  <br/> |<span data-ttu-id="f5271-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="f5271-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="f5271-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f5271-112">Row index:</span></span>  <br/> |<span data-ttu-id="f5271-113">**visRowProp +** *i*  где  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f5271-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f5271-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f5271-114">Cell index:</span></span>  <br/> |<span data-ttu-id="f5271-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="f5271-115">**visCustPropsPrompt**</span></span> <br/> |
   

