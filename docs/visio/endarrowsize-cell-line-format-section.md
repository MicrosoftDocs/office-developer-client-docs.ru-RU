---
title: Ячейка EndArrowSize (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Определяет размер стрелки в конце строки.
ms.openlocfilehash: e03871c75857297634300c2eee091de2d0144903
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813708"
---
# <a name="endarrowsize-cell-line-format-section"></a>Ячейка EndArrowSize (раздел "Формат линий")

Определяет размер стрелки в конце строки.
  
|**Значение**|**Size**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Очень маленькие  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Малый  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Средний  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Большая  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Очень большой  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |Большие  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |Колоссальных  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение в поле **строка** (на вкладке **Главная** в группе **фигуру** щелкните **строку**, выберите пункт **стрелки**и нажмите кнопку **Дополнительно стрелки**).
  
Чтобы получить ссылку на ячейку EndArrowSize по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |EndArrowSize  <br/> |
   
Для получения ссылки на ячейки EndArrowSize по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineEndArrowSize** <br/> |
   

