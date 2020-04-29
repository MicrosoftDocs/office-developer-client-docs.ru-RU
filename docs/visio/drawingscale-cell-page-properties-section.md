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
description: Представляет значение единицы документа в текущем масштабе документа. Масштаб документа для страницы — это отношение единицы страницы, показанной в ячейке PageScale, к единице измерения, показанной в ячейке DrawingScale.
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413320"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="e321b-104">DrawingScale Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="e321b-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="e321b-105">Представляет значение единицы документа в текущем масштабе документа.</span><span class="sxs-lookup"><span data-stu-id="e321b-105">Represents the value of the drawing unit in the current drawing scale.</span></span> <span data-ttu-id="e321b-106">Масштаб документа для страницы — это отношение единицы страницы, показанной в ячейке PageScale, к единице измерения, показанной в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e321b-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="e321b-107">Можно задать ячейку DrawingScale, чтобы изменить единицы измерения линеек страницы из программы.</span><span class="sxs-lookup"><span data-stu-id="e321b-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="e321b-108">Ниже приведен пример изменения единиц измерения с дюймов на сантиметры из программы.</span><span class="sxs-lookup"><span data-stu-id="e321b-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="e321b-109">В этом случае мы используем метод **конвертресулт** для хранения одинакового расстояния, но выражают его в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="e321b-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="e321b-110">Вы можете определить систему измерения в документе, изучив свойство **Units** ячейки DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e321b-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="e321b-111">После выполнения приведенного выше макроса следующий оператор, выполняемый в окне интерпретации редактора Visual Basic, возвратит *значение true* .</span><span class="sxs-lookup"><span data-stu-id="e321b-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="e321b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e321b-112">Remarks</span></span>

<span data-ttu-id="e321b-113">Эта ячейка соответствует параметрам в диалоговом окне "Параметры **страницы** " (щелкните стрелку **настройки страницы** на вкладке " **Главная** ").</span><span class="sxs-lookup"><span data-stu-id="e321b-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="e321b-114">Единицы измерения формулы в ячейке DrawingScale определяют единицы измерения, используемые линейками в окне документа.</span><span class="sxs-lookup"><span data-stu-id="e321b-114">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window.</span></span> <span data-ttu-id="e321b-115">Если не требуется изменять масштаб документа, можно выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="e321b-115">If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="e321b-116">Не изменяйте расстояние, выраженное в ячейке DrawingScale, но выражает его в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="e321b-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="e321b-117">Измените расстояние, выраженное в ячейке PageScale, на тот же фактор, который вы изменили DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="e321b-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="e321b-118">Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e321b-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e321b-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e321b-119">Cell name:</span></span>  <br/> |<span data-ttu-id="e321b-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="e321b-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="e321b-121">Чтобы получить ссылку на ячейку DrawingScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e321b-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e321b-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e321b-122">Section index:</span></span>  <br/> |<span data-ttu-id="e321b-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e321b-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e321b-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e321b-124">Row index:</span></span>  <br/> |<span data-ttu-id="e321b-125">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="e321b-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="e321b-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e321b-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e321b-127">**виспажедравингскале**</span><span class="sxs-lookup"><span data-stu-id="e321b-127">**visPageDrawingScale**</span></span> <br/> |
   

