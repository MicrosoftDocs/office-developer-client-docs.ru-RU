---
title: Ячейка ShapeRouteStyle (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Определяет стиль маршрута и направление указанной соединительной линии на странице документа.
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814787"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Ячейка ShapeRouteStyle (раздел "Макет фигуры")

Определяет стиль маршрута и направление указанной соединительной линии на странице документа.
  
|**Значение**|**Стиль маршрута**|**Direction**|**Константа автоматизации**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Использование страницы по умолчанию  <br/> |Нет  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Правая угловая  <br/> |Нет  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Прямой  <br/> |Нет  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Организационная диаграмма  <br/> |Сверху вниз  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Организационная диаграмма  <br/> |Слева направо  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Блок-схема  <br/> |Сверху вниз  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Блок-схема  <br/> |Слева направо  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |Дерево  <br/> |Сверху вниз  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Дерево  <br/> |Слева направо  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Сеть  <br/> |Нет  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Организационная диаграмма  <br/> |Снизу вверх  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Организационная диаграмма  <br/> |Справа налево  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Блок-схема  <br/> |Снизу вверх  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Блок-схема  <br/> |Справа налево  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Дерево  <br/> |Снизу вверх  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Дерево  <br/> |Справа налево  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |Центр обработки центр  <br/> |Нет  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |Простое  <br/> |Сверху вниз  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |Простое  <br/> |Слева направо  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Простое  <br/> |Снизу вверх  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Простое  <br/> |Справа налево  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Простой по горизонтали-по вертикали  <br/> |Нет  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Простой по вертикали-по горизонтали  <br/> |Нет  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Замечания

Можно также задать значение ячейки для отдельного соединителя на вкладке **соединителя** в диалоговом окне " **поведение** " (с выбранного соединения щелкните **поведение** на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) и затем перейдите на вкладку **соединителя** ). 
  
Чтобы задать это поведение для *всех* соединителей на странице, используйте RouteStyle ячейки в разделе макет страницы. 
  
Более ранних чем Visio 2000 в версиях задайте это поведение, с помощью ObjBehavior ячеек в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapeRouteStyle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapeRouteStyle  <br/> |
   
Для получения ссылки на ячейки ShapeRouteStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLORouteStyle** <br/> |
   

