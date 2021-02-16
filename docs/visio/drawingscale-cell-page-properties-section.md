---
title: DrawingScale Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Представляет значение единицы рисования в текущей шкале рисования. Масштаб рисования для страницы — это соотношение единицы страницы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413320"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="e9bc4-104">DrawingScale Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="e9bc4-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="e9bc4-105">Представляет значение единицы рисования в текущей шкале рисования.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-105">Represents the value of the drawing unit in the current drawing scale.</span></span> <span data-ttu-id="e9bc4-106">Масштаб рисования для страницы — это соотношение единицы страницы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="e9bc4-107">Вы можете настроить ячейку DrawingScale, чтобы изменить единицы линейки страницы из программы.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="e9bc4-108">Вот пример изменения единиц измерения из дюйма в см от программы.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="e9bc4-109">В этом случае мы используем метод **ConvertResult,** чтобы оставить расстояние таким же, но выразить его в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="e9bc4-110">Систему показателей можно определить на рисунке, изучив свойство **Units** ячейки DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="e9bc4-111">После выполнения вышеуказанного макроса следующий выписка, выполненная в окне Visual Basic "Immediate" редактора, возвращает *true.*</span><span class="sxs-lookup"><span data-stu-id="e9bc4-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="e9bc4-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9bc4-112">Remarks</span></span>

<span data-ttu-id="e9bc4-113">Эта ячейка соответствует настройкам  в диалоговом окне "Настройка страницы" (щелкните стрелку "Настройка **страницы"** на вкладке **"Главная").**</span><span class="sxs-lookup"><span data-stu-id="e9bc4-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="e9bc4-114">Единицы формулы в ячейке DrawingScale определяют единицы измерения, используемые линейками в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-114">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window.</span></span> <span data-ttu-id="e9bc4-115">Если вы не хотите изменять масштаб рисунка, можно сделать одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-115">If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="e9bc4-116">Сохраняем расстояние, выраженное в ячейке DrawingScale, но выражая его в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="e9bc4-117">Измените расстояние, выраженное в ячейке PageScale, на тот же фактор, что и при изменении DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="e9bc4-118">Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9bc4-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-119">Cell name:</span></span>  <br/> |<span data-ttu-id="e9bc4-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="e9bc4-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="e9bc4-121">Чтобы получить ссылку на ячейку DrawingScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9bc4-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-122">Section index:</span></span>  <br/> |<span data-ttu-id="e9bc4-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9bc4-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e9bc4-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-124">Row index:</span></span>  <br/> |<span data-ttu-id="e9bc4-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e9bc4-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="e9bc4-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e9bc4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e9bc4-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="e9bc4-127">**visPageDrawingScale**</span></span> <br/> |
   

