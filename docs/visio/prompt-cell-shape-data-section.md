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
description: Указывает описательный или пояснительный текст, который отображается в виде подсказки при приостановке указателя мыши над значением в окне Данные фигуры.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326819"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="8b56b-103">Prompt Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="8b56b-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="8b56b-104">Указывает описательный или пояснительный текст, который отображается в виде подсказки при приостановке указателя мыши над значением в окне **данные фигуры** .</span><span class="sxs-lookup"><span data-stu-id="8b56b-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8b56b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b56b-105">Remarks</span></span>

<span data-ttu-id="8b56b-106">Чтобы получить ссылку на ячейку приглашения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8b56b-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b56b-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b56b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="8b56b-108">Установите.  *Name (имя* ). ПодСказка, где *Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="8b56b-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8b56b-109">Чтобы получить ссылку на ячейку приглашения по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8b56b-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b56b-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b56b-110">Section index:</span></span>  <br/> |<span data-ttu-id="8b56b-111">**Виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="8b56b-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="8b56b-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b56b-112">Row index:</span></span>  <br/> |<span data-ttu-id="8b56b-113">**висровпроп +** \*\* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8b56b-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8b56b-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b56b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="8b56b-115">**Вискустпропспромпт**</span><span class="sxs-lookup"><span data-stu-id="8b56b-115">**visCustPropsPrompt**</span></span> <br/> |
   

