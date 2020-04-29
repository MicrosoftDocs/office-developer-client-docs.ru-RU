---
title: PageScale Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Определяет значение единицы страницы в текущем масштабе документа. Масштаб документа для страницы — это отношение единицы страницы, показанной в ячейке PageScale, к единице измерения, показанной в ячейке DrawingScale.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405536"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="75e61-104">PageScale Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="75e61-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="75e61-105">Определяет значение единицы страницы в текущем масштабе документа.</span><span class="sxs-lookup"><span data-stu-id="75e61-105">Determines the value of the page unit in the current drawing scale.</span></span> <span data-ttu-id="75e61-106">Масштаб документа для страницы — это отношение единицы страницы, показанной в ячейке PageScale, к единице измерения, показанной в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="75e61-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75e61-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="75e61-107">Remarks</span></span>

<span data-ttu-id="75e61-108">Кроме того, можно задать значение ячейки PageScale на вкладке **шкала документа** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="75e61-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="75e61-109">Ячейка является первым из двух чисел в **предварительно заданном поле масштабирования** или **настраиваемой шкале** , в зависимости от параметра масштабирования документа, выбранного в разделе **масштаб документа**.</span><span class="sxs-lookup"><span data-stu-id="75e61-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="75e61-110">Например, если выбрать архитектурный масштаб для документа, то масштаб рисунка для страницы будет 3/32 "= 1" 0 ".</span><span class="sxs-lookup"><span data-stu-id="75e61-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="75e61-111">Значение в ячейке PageScale равно 0,0938.</span><span class="sxs-lookup"><span data-stu-id="75e61-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="75e61-112">(или 3/32 "), а значение в ячейке DrawingScale — 1 ФТ.</span><span class="sxs-lookup"><span data-stu-id="75e61-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="75e61-113">Чтобы получить ссылку на ячейку PageScale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="75e61-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75e61-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="75e61-114">Cell name:</span></span>  <br/> |<span data-ttu-id="75e61-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="75e61-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="75e61-116">Чтобы получить ссылку на ячейку PageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="75e61-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75e61-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="75e61-117">Section index:</span></span>  <br/> |<span data-ttu-id="75e61-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75e61-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="75e61-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="75e61-119">Row index:</span></span>  <br/> |<span data-ttu-id="75e61-120">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="75e61-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="75e61-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="75e61-121">Cell index:</span></span>  <br/> |<span data-ttu-id="75e61-122">**виспажескале**</span><span class="sxs-lookup"><span data-stu-id="75e61-122">**visPageScale**</span></span> <br/> |
   

