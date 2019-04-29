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
description: Определяет размер наконечника в конце строки.
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438080"
---
# <a name="endarrowsize-cell-line-format-section"></a>EndArrowSize Cell (Line Format Section)

Определяет размер наконечника в конце строки.
  
|**Значение**|**Size**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Очень маленький  <br/> |**Висарровсизеверисмалл** <br/> |
|1,1  <br/> |Малый  <br/> |**Висарровсизесмалл** <br/> |
|2  <br/> |Средняя  <br/> |**Висарровсиземедиум** <br/> |
|4  <br/> |Крупный  <br/> |**Висарровсизеларже** <br/> |
|SP4  <br/> |Сверхбольшой  <br/> |**Висарровсизевериларже** <br/> |
|17:00  <br/> |Круп  <br/> |**Висарровсизежумбо** <br/> |
|ICMPv6  <br/> |Колоссал  <br/> |**Висарровсизеколоссал** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете задать это значение в диалоговом окне **строка** (на вкладке **Главная** , в группе Группа **** , затем последовательно выберите пункты **линия**и **стрелки**и **Другие стрелки**).
  
Чтобы получить ссылку на ячейку EndArrowSize по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EndArrowSize  <br/> |
   
Чтобы получить ссылку на ячейку EndArrowSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровлине** <br/> |
|Индекс ячейки:  <br/> |**Вислининдарровсизе** <br/> |
   

