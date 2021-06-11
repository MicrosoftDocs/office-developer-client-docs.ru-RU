---
title: Tip Cell (Controls Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Представляет текстовую строку описательной, которая появляется в виде подсказки инструмента, когда пользователь приостанавливирует указатель над ручкой управления фигурой. Приложение автоматически заключит строку подсказки в кавычках в ячейке, но кавычка не отображается в подсказке инструмента.
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424863"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="01154-104">Tip Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="01154-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="01154-105">Представляет текстовую строку описательной, которая появляется в виде подсказки инструмента, когда пользователь приостанавливирует указатель над ручкой управления фигурой.</span><span class="sxs-lookup"><span data-stu-id="01154-105">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle.</span></span> <span data-ttu-id="01154-106">Приложение автоматически заключит строку подсказки в кавычках в ячейке, но кавычка не отображается в подсказке инструмента.</span><span class="sxs-lookup"><span data-stu-id="01154-106">The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01154-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="01154-107">Remarks</span></span>

<span data-ttu-id="01154-108">Чтобы получить ссылку на ячейку Подсказка по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="01154-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01154-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="01154-109">Cell name:</span></span>  <br/> | <span data-ttu-id="01154-110">Controls.</span><span class="sxs-lookup"><span data-stu-id="01154-110">Controls.</span></span>  <span data-ttu-id="01154-111">*имя*  . Элементы управления Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="01154-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="01154-112">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="01154-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="01154-113">Чтобы получить ссылку на ячейку Подсказка по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="01154-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01154-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="01154-114">Section index:</span></span>  <br/> |<span data-ttu-id="01154-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="01154-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="01154-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="01154-116">Row index:</span></span>  <br/> |<span data-ttu-id="01154-117">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="01154-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="01154-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="01154-118">Cell index:</span></span>  <br/> |<span data-ttu-id="01154-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="01154-119">**visCtlTip**</span></span> <br/> |
   

