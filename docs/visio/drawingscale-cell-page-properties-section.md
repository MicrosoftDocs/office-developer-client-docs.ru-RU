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
# <a name="drawingscale-cell-page-properties-section"></a>DrawingScale Cell (Page Properties Section)

Представляет значение единицы рисования в текущей шкале рисования. Масштаб рисования для страницы — это соотношение единицы страницы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.
  
Вы можете настроить ячейку DrawingScale, чтобы изменить единицы линейки страницы из программы. Вот пример изменения единиц измерения из дюйма в см от программы. В этом случае мы используем метод **ConvertResult,** чтобы оставить расстояние таким же, но выразить его в разных единицах. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Систему показателей можно определить на рисунке, изучив свойство **Units** ячейки DrawingScale. После выполнения вышеуказанного макроса следующий выписка, выполненная в окне Visual Basic "Immediate" редактора, возвращает *true.* 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Примечания

Эта ячейка соответствует настройкам  в диалоговом окне "Настройка страницы" (щелкните стрелку "Настройка **страницы"** на вкладке **"Главная").** 
  
Единицы формулы в ячейке DrawingScale определяют единицы измерения, используемые линейками в окне рисования. Если вы не хотите изменять масштаб рисунка, можно сделать одно из следующих:
  
- Сохраняем расстояние, выраженное в ячейке DrawingScale, но выражая его в разных единицах.
    
- Измените расстояние, выраженное в ячейке PageScale, на тот же фактор, что и при изменении DrawingScale.
    
Чтобы получить ссылку на ячейку DrawingScale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |DrawingScale  <br/> |
   
Чтобы получить ссылку на ячейку DrawingScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageDrawingScale** <br/> |
   

