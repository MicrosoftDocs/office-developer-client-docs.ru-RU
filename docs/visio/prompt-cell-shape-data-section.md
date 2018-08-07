---
title: Ячейка Prompt (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Задает описательный или управляющий текст, который отображается в виде подсказки при наведении курсора на значение в окне данных фигуры.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814486"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="8b6f2-103">Ячейка Prompt (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="8b6f2-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="8b6f2-104">Задает описательный или управляющий текст, который отображается в виде подсказки при наведении курсора на значение в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="8b6f2-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8b6f2-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b6f2-105">Remarks</span></span>

<span data-ttu-id="8b6f2-106">Для получения ссылки на ячейки приглашениями по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8b6f2-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b6f2-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8b6f2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="8b6f2-108">Свойства.  *Имя* . Запрос, где *имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="8b6f2-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8b6f2-109">Для получения ссылки на ячейки приглашениями по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8b6f2-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b6f2-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b6f2-110">Section index:</span></span>  <br/> |<span data-ttu-id="8b6f2-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="8b6f2-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="8b6f2-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b6f2-112">Row index:</span></span>  <br/> |<span data-ttu-id="8b6f2-113">**visRowProp +** *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8b6f2-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8b6f2-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b6f2-114">Cell index:</span></span>  <br/> |<span data-ttu-id="8b6f2-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="8b6f2-115">**visCustPropsPrompt**</span></span> <br/> |
   

