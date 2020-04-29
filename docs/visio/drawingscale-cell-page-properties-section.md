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
# <a name="drawingscale-cell-page-properties-section"></a>DrawingScale Cell (Page Properties Section)

Представляет значение единицы документа в текущем масштабе документа. Масштаб документа для страницы — это отношение единицы страницы, показанной в ячейке PageScale, к единице измерения, показанной в ячейке DrawingScale.
  
Можно задать ячейку DrawingScale, чтобы изменить единицы измерения линеек страницы из программы. Ниже приведен пример изменения единиц измерения с дюймов на сантиметры из программы. В этом случае мы используем метод **конвертресулт** для хранения одинакового расстояния, но выражают его в разных единицах. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Вы можете определить систему измерения в документе, изучив свойство **Units** ячейки DrawingScale. После выполнения приведенного выше макроса следующий оператор, выполняемый в окне интерпретации редактора Visual Basic, возвратит *значение true* . 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Примечания

Эта ячейка соответствует параметрам в диалоговом окне "Параметры **страницы** " (щелкните стрелку **настройки страницы** на вкладке " **Главная** "). 
  
Единицы измерения формулы в ячейке DrawingScale определяют единицы измерения, используемые линейками в окне документа. Если не требуется изменять масштаб документа, можно выполнить одно из следующих действий:
  
- Не изменяйте расстояние, выраженное в ячейке DrawingScale, но выражает его в разных единицах.
    
- Измените расстояние, выраженное в ячейке PageScale, на тот же фактор, который вы изменили DrawingScale.
    
Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DrawingScale  <br/> |
   
Чтобы получить ссылку на ячейку DrawingScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровпаже** <br/> |
|Индекс ячейки:  <br/> |**виспажедравингскале** <br/> |
   

