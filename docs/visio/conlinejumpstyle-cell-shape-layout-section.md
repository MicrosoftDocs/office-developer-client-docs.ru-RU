---
title: ConLineJumpStyle Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Определяет стиль значка пересечения линий для перемычек на динамическом соединителе.
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360062"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle Cell (Shape Layout Section)

Определяет стиль значка пересечения линий для перемычек на динамическом соединителе.
  
|**Значение**|**Стиль значка пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Страница по умолчанию  <br/> |**Висложумпстиледефаулт** <br/> |
|1,1  <br/> |Гипербол  <br/> |**Висложумпстилеарк** <br/> |
|2  <br/> |Gap  <br/> |**Висложумпстилегап** <br/> |
|4  <br/> |Го  <br/> |**Висложумпстилескуаре** <br/> |
|SP4  <br/> |Треугольник  <br/> |**Висложумпстилетриангле** <br/> |
|17:00  <br/> |3 стороны  <br/> |**visLOJumpStyle2Point** <br/> |
|ICMPv6  <br/> |4 стороны  <br/> |**visLOJumpStyle3Point** <br/> |
|см  <br/> |5 Сторон  <br/> |**visLOJumpStyle4Point** <br/> |
|8,5  <br/> |6 сторон  <br/> |**visLOJumpStyle5Point** <br/> |
|10  <br/> |7 Сторон  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровшапелайаут** <br/> |
|Индекс ячейки:  <br/> |**Виссложумпстиле** <br/> |
   
## <a name="remarks"></a>Примечания

Можно также задать значение этой ячейки, выбрав динамический соединитель, нажав кнопку **поведение** в группе **Макет фигуры** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем щелкнув вкладку **соединитель** . 
  
Чтобы получить ссылку на ячейку ConLineJumpStyle по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ConLineJumpStyle  <br/> |
   
Чтобы получить ссылку на ячейку ConLineJumpStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  

