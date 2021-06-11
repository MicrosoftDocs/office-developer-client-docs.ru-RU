---
title: RouteStyle Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Определяет стиль маршрутивки и направление для всех соединители на странице рисования, которые не имеют локального стиля маршрутивки.
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424786"
---
# <a name="routestyle-cell-page-layout-section"></a>RouteStyle Cell (Page Layout Section)

Определяет стиль маршрутивки и направление для всех соединители на странице рисования, которые не имеют локального стиля маршрутивки.
  
|**Значение**|**Стиль маршрутивки**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|:-----|
|0  <br/> |По умолчанию; правый угол  <br/> |Нет  <br/> |**visLORouteDefault** <br/> |
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

Вы также можете установить значение этой  ячейки на вкладке Макет и маршрутинг  в диалоговом  окне Установка страницы (на вкладке Дизайн нажмите стрелку установки страницы, нажмите макет и маршрутику, а затем щелкните **Spacing** ).   
  
В ячейке ShapeRouteStyle раздела Макет фигуры можно установить локальный стиль маршрутивки для соединителя. 
  
Чтобы получить ссылку на ячейку RouteStyle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |RouteStyle  <br/> |
   
Чтобы получить ссылку на ячейку RouteStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLORouteStyle** <br/> |
   

