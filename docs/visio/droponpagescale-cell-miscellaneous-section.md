---
title: DropOnPageScale Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359663"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>DropOnPageScale Cell (Miscellaneous Section)

Содержит процентное значение, на которое масштабирована фигура при удалении на странице документа.
  
## <a name="remarks"></a>Примечания

В следующих двух случаях Visio масштабирует фигуры таким образом, чтобы они правильно отображались на странице документа:
  
- При перетаскивании неизмеренных фигур на масштабируемые рисунки.
    
- При отбрасывания измерений фигуры отправляются на немасштабированные рисунки.
    
Процент в ячейке DropOnPageScale указывает коэффициент, на который Visio Масштабирует фигуру (\>100) или вниз (\<100). Этот номер можно использовать как фактор при расчете жестко запрограммированных значений. 
  
Это значение равно 100% для измеренных фигур на масштабированных рисунках или неизмеренных фигур на немасштабированных рисунках. 
  
Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DropOnPageScale  <br/> |
   
Чтобы получить ссылку на ячейку DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровмиск** <br/> |
| Индекс ячейки:  <br/> |**Висобждропонпажескале** <br/> |
   

