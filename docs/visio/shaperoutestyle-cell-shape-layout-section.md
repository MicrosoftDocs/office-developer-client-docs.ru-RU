---
title: ShapeRouteStyle Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Определяет стиль маршрутики и направление выбранного соединитетеля на странице рисования.
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425031"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>ShapeRouteStyle Cell (Shape Layout Section)

Определяет стиль маршрутики и направление выбранного соединитетеля на странице рисования.
  
|**Значение**|**Стиль маршрутивки**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Использование по умолчанию страницы  <br/> |Нет  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Правый угол  <br/> |Нет  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Прямая  <br/> |Нет  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Диаграмма организации  <br/> |Сверху вниз  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |Диаграмма организации  <br/> |Слева направо  <br/> |**visLORouteOrgChartWE** <br/> |
|5   <br/> |Блок-схема  <br/> |Сверху вниз  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Блок-схема  <br/> |Слева направо  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Дерево  <br/> |Сверху вниз  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Дерево  <br/> |Слева направо  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Сеть  <br/> |Нет  <br/> |**visLORouteNetwork** <br/> |
|10   <br/> |Диаграмма организации  <br/> |Снизу вверх  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Диаграмма организации  <br/> |Справа налево  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Блок-схема  <br/> |Снизу вверх  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Блок-схема  <br/> |Справа налево  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Дерево  <br/> |Снизу вверх  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Дерево  <br/> |Справа налево  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |Центр в центр  <br/> |Нет  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Простой  <br/> |Сверху вниз  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Простой  <br/> |Слева направо  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Простой  <br/> |Снизу вверх  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Простой  <br/> |Справа налево  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Простая горизонтально-вертикаль  <br/> |Нет  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Простая вертикально-горизонтальная  <br/> |Нет  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки для определенного соединитетеля на вкладке **Соединитель** в  диалоговом [](run-in-developer-mode-display-the-developer-tab.md) окне Поведение (с выбранным соединитетелем щелкните Поведение на вкладке Разработчик, а затем нажмите вкладку **Соединитель).**  
  
Чтобы установить такое поведение  *для всех*  соединителей на странице, используйте ячейку RouteStyle в разделе Макет страницы. 
  
В версиях, ранее Visio 2000 г., вы установите такое поведение с помощью ячейки ObjBehavior в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapeRouteStyle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapeRouteStyle  <br/> |
   
Чтобы получить ссылку на ячейку ShapeRouteStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLORouteStyle** <br/> |
   

