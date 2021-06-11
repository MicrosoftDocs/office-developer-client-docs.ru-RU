---
title: ShapeFixedCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Указывает поведение размещения для размещения фигуры.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431745"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>ShapeFixedCode Cell (Shape Layout Section)

Указывает поведение размещения для размещения фигуры.
  
|**Значение**|**Режим выбора**|**Константа автоматизации**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Не перемещайте эту фигуру, когда фигуры выложены с помощью диалогового окна **Configure Layout.**  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Не двигайте эту фигуру и не позволяйте фигурам, которые вспахить, помещать поверх нее.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Не перемещайте эту фигуру и не позволяйте фигурам, которые вспахить, помещать поверх нее.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Игнорируйте расположения точек подключения при маршруте.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Только разрешить маршрутику в стороны с точками подключения.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Не приклеить к периметру этой фигуры. Вместо этого приклейте к окне выравнивания фигуры.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой  ячейки  на вкладке Размещение в диалоговом [](run-in-developer-mode-display-the-developer-tab.md) окне Поведение (с выбранной фигурой на вкладке Разработчик, в группе **Shape Design** нажмите кнопку **Поведение,** а затем щелкните вкладку **Размещение).** 
  
Вы можете установить любое сочетание этих значений для этой ячейки. Например, можно ввести значение 3 (H3), которое исключает движение при выкладке фигур с помощью диалогового окна Configure Layout (на вкладке Design, в группе Макет, щелкните страницу повторной макета, а затем нажмите кнопку Дополнительные параметры макета) и при размещении других фигур на или вблизи &amp; фигуры.      
  
В версиях до Visio 2000 года такое поведение устанавливается с помощью ячейки ObjInteract в разделе Разное. 
  
Чтобы получить ссылку на ячейку ShapeFixedCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapeFixedCode  <br/> |
   
Чтобы получить ссылку на ячейку ShapeFixedCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOFixedCode** <br/> |
   

