---
title: EndArrowSize Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Определяет размер наконечник стрелки в конце строки.
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438080"
---
# <a name="endarrowsize-cell-line-format-section"></a>EndArrowSize Cell (Line Format Section)

Определяет размер наконечник стрелки в конце строки.
  
|**Значение**|**Размер**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Очень маленький  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Малый  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Средний  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Крупный  <br/> |**visArrowSizeLarge** <br/> |
|4   <br/> |Сверхбольшой  <br/> |**visArrowSizeVeryLarge** <br/> |
|5   <br/> |Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
|6   <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение в диалоговом окне **Line** (на вкладке **Главная,** в группе **Shape** нажмите кнопку **Line,** указать стрелки, а затем нажмите кнопку **Дополнительные стрелки).**
  
Чтобы получить ссылку на ячейку EndArrowSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EndArrowSize  <br/> |
   
Чтобы получить ссылку на ячейку EndArrowSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLineEndArrowSize** <br/> |
   

