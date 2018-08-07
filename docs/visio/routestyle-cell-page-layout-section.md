---
title: Ячейка RouteStyle (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Определяет стиль маршрута и направление для всех соединителей на странице документа, не имеющих локальных стилей маршрута.
ms.openlocfilehash: d64e7b3c7cf30f0a657ede57b227acefd4b10101
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814649"
---
# <a name="routestyle-cell-page-layout-section"></a>Ячейка RouteStyle (раздел "Макет страницы")

Определяет стиль маршрута и направление для всех соединителей на странице документа, не имеющих локальных стилей маршрута.
  
|**Значение**|**Стиль маршрута**|**Direction**|**Константа автоматизации**|
|:-----|:-----|:-----|:-----|
|0  <br/> |По умолчанию; правая угловая  <br/> |Нет  <br/> |**visLORouteDefault** <br/> |
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

Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладке **Конструктор** щелкните стрелку **Параметры страницы** , нажмите кнопку **Макет и маршрутизации**и нажмите кнопку **интервала** ). 
  
Можно задать локальных стилей маршрута для соединителя в ячейке ShapeRouteStyle раздел макет фигуры. 
  
Чтобы получить ссылку на ячейку RouteStyle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |RouteStyle  <br/> |
   
Для получения ссылки на ячейки RouteStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLORouteStyle** <br/> |
   

