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
# <a name="drawingscale-cell-page-properties-section"></a>Ячейка DrawingScale (раздел "Свойства страницы")

Представляет значение единице документа в текущем масштабе документа. Масштаб документа для страницы представляет собой отношение единицы страницы в ячейке PageScale к единице документа в ячейке DrawingScale.
  
Можно задать ячейке DrawingScale Изменение единицы линейки страницы из программы. Ниже приведен пример Изменение единиц измерения с дюймов на см из программы. В этом случае мы используем метод **ConvertResult** , чтобы сохранить расстояние же, но express в разных единицах. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Системы измерений в документе можно определить, проверив свойство **единицы** DrawingScale ячейки. После выполнения выше макроса в редакторе Visual Basic Интерпретация следующий оператор окно вернет *значение True* . 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Замечания

В этой ячейке соответствует параметры в диалоговом окне **Параметры страницы** (щелкните стрелку **Параметры страницы** на вкладке **Главная** ). 
  
Единицы формулы в ячейке DrawingScale определить единицы измерения, используемые линейки в окне документа. Если вы не хотите также изменить масштаб документа, можно выполнить одно из следующих:
  
- Keep расстояние выражается в ячейке DrawingScale же, но express в разных единицах.
    
- Измените расстояние, выраженная в ячейке PageScale с одной коэффициента изменении DrawingScale.
    
Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |DrawingScale  <br/> |
   
Для получения ссылки на ячейки DrawingScale по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageDrawingScale** <br/> |
   

