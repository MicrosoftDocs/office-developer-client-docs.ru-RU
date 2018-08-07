---
title: Ячейка DrawingScale (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Представляет значение единице документа в текущем масштабе документа. Масштаб документа для страницы представляет собой отношение единицы страницы в ячейке PageScale к единице документа в ячейке DrawingScale.
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813641"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="b5a9c-104">Ячейка DrawingScale (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="b5a9c-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="b5a9c-105">Представляет значение единице документа в текущем масштабе документа.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-105">Represents the value of the drawing unit in the current drawing scale.</span></span> <span data-ttu-id="b5a9c-106">Масштаб документа для страницы представляет собой отношение единицы страницы в ячейке PageScale к единице документа в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="b5a9c-107">Можно задать ячейке DrawingScale Изменение единицы линейки страницы из программы.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="b5a9c-108">Ниже приведен пример Изменение единиц измерения с дюймов на см из программы.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="b5a9c-109">В этом случае мы используем метод **ConvertResult** , чтобы сохранить расстояние же, но express в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="b5a9c-110">Системы измерений в документе можно определить, проверив свойство **единицы** DrawingScale ячейки.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="b5a9c-111">После выполнения выше макроса в редакторе Visual Basic Интерпретация следующий оператор окно вернет *значение True* .</span><span class="sxs-lookup"><span data-stu-id="b5a9c-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="b5a9c-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5a9c-112">Remarks</span></span>

<span data-ttu-id="b5a9c-113">В этой ячейке соответствует параметры в диалоговом окне **Параметры страницы** (щелкните стрелку **Параметры страницы** на вкладке **Главная** ).</span><span class="sxs-lookup"><span data-stu-id="b5a9c-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="b5a9c-114">Единицы формулы в ячейке DrawingScale определить единицы измерения, используемые линейки в окне документа.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-114">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window.</span></span> <span data-ttu-id="b5a9c-115">Если вы не хотите также изменить масштаб документа, можно выполнить одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-115">If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="b5a9c-116">Keep расстояние выражается в ячейке DrawingScale же, но express в разных единицах.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="b5a9c-117">Измените расстояние, выраженная в ячейке PageScale с одной коэффициента изменении DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="b5a9c-118">Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5a9c-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-119">Cell name:</span></span>  <br/> |<span data-ttu-id="b5a9c-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="b5a9c-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="b5a9c-121">Для получения ссылки на ячейки DrawingScale по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5a9c-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-122">Section index:</span></span>  <br/> |<span data-ttu-id="b5a9c-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b5a9c-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-124">Row index:</span></span>  <br/> |<span data-ttu-id="b5a9c-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="b5a9c-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b5a9c-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b5a9c-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-127">**visPageDrawingScale**</span></span> <br/> |
   

