---
title: BeginArrowSize Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Определяет размер наконечника в начале линии.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346230"
---
# <a name="beginarrowsize-cell-line-format-section"></a>BeginArrowSize Cell (Line Format Section)

Определяет размер наконечника в начале линии.
  
|**Значение**|**Size**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Очень маленький  <br/> |**Висарровсизеверисмалл** <br/> |
| 1,1  <br/> | НАИМЕНЬШИЙ  <br/> |**Висарровсизесмалл** <br/> |
| 2  <br/> | Средние  <br/> |**Висарровсиземедиум** <br/> |
| 4  <br/> | НАИБОЛЬШИЙ  <br/> |**Висарровсизеларже** <br/> |
| SP4  <br/> | Очень крупный  <br/> |**Висарровсизевериларже** <br/> |
| 17:00  <br/> | Круп  <br/> |**Висарровсизежумбо** <br/> |
| ICMPv6  <br/> | Колоссал  <br/> |**Висарровсизеколоссал** <br/> |
   
## <a name="remarks"></a>Комментарии

Вы также можете задать размер наконечника в диалоговом окне " **линия** ". 
  
Чтобы получить ссылку на ячейку BeginArrowSize по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BeginArrowSize  <br/> |
   
Чтобы получить ссылку на ячейку BeginArrowSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлине** <br/> |
| Индекс ячейки:  <br/> |**Вислинебегинарровсизе** <br/> |
   

