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
description: Определяет значение единицы страницы в текущей шкале рисования. Масштаб рисования для страницы — это соотношение единицы страницы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405536"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="8722d-104">PageScale Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="8722d-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="8722d-105">Определяет значение единицы страницы в текущей шкале рисования.</span><span class="sxs-lookup"><span data-stu-id="8722d-105">Determines the value of the page unit in the current drawing scale.</span></span> <span data-ttu-id="8722d-106">Масштаб рисования для страницы — это соотношение единицы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="8722d-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8722d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="8722d-107">Remarks</span></span>

<span data-ttu-id="8722d-108">Вы также можете установить значение ячейки  PageScale на  вкладке "Масштаб рисования" в диалоговом окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку **"Настройка** страницы"). </span><span class="sxs-lookup"><span data-stu-id="8722d-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="8722d-109">Значение ячейки является первым из двух чисел в предварительно определенном поле шкалы или настраиваемом поле масштабирования в зависимости от параметра масштабирования рисования, выбранного в масштабе **рисования.**  </span><span class="sxs-lookup"><span data-stu-id="8722d-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="8722d-110">Например, если вы выбрали архитектурную шкалу для своего рисунка, то масштаб рисования для страницы будет 3/32" = 1'0".</span><span class="sxs-lookup"><span data-stu-id="8722d-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="8722d-111">Значение в ячейке PageScale — 0,0938.</span><span class="sxs-lookup"><span data-stu-id="8722d-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="8722d-112">(или 3/32") и значение в ячейке DrawingScale составляет 1 ft.</span><span class="sxs-lookup"><span data-stu-id="8722d-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="8722d-113">Чтобы получить ссылку на ячейку PageScale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8722d-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8722d-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8722d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="8722d-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="8722d-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="8722d-116">Чтобы получить ссылку на ячейку PageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8722d-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8722d-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8722d-117">Section index:</span></span>  <br/> |<span data-ttu-id="8722d-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8722d-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8722d-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8722d-119">Row index:</span></span>  <br/> |<span data-ttu-id="8722d-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="8722d-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="8722d-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8722d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="8722d-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="8722d-122">**visPageScale**</span></span> <br/> |
   

