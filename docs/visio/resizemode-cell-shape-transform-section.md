---
title: ResizeMode Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Показывает текущее поведение изменения размеров фигуры.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421965"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode Cell (Shape Transform Section)

Показывает текущее поведение изменения размеров фигуры.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Используйте параметр группы.  <br/> |**visXFormResizeDontCare** <br/> |
|1   <br/> |Только для перенастройки.  <br/> |**visXFormResizeSpread** <br/> |
|2   <br/> |Масштабировать с помощью группы.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение  на вкладке **"Поведение"** в диалоговом окне "Поведение" (на вкладке "Разработчик" в группе "Проектирование фигур" щелкните [](run-in-developer-mode-display-the-developer-tab.md) **"Поведение").**  Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ResizeMode  <br/> |
   
Чтобы получить ссылку на ячейку ResizeMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowXFormOut** <br/> |
|Индекс ячейки:  <br/> |**visXFormResizeMode** <br/> |
   

