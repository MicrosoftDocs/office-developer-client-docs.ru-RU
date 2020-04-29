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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412284"
---
# <a name="beginarrowsize-cell-line-format-section"></a>BeginArrowSize Cell (Line Format Section)

Определяет размер наконечника в начале линии.
  
|**Значение**|**Размер**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Очень маленький  <br/> |**висарровсизеверисмалл** <br/> |
| 1,1  <br/> | Малый  <br/> |**висарровсизесмалл** <br/> |
| 2  <br/> | Средние  <br/> |**висарровсиземедиум** <br/> |
| 4  <br/> | Большой  <br/> |**висарровсизеларже** <br/> |
| 4   <br/> | Очень крупный  <br/> |**висарровсизевериларже** <br/> |
| 5   <br/> | Круп  <br/> |**висарровсизежумбо** <br/> |
| 6   <br/> | колоссал  <br/> |**висарровсизеколоссал** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете задать размер наконечника в диалоговом окне " **линия** ". 
  
Чтобы получить ссылку на ячейку BeginArrowSize по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BeginArrowSize  <br/> |
   
Чтобы получить ссылку на ячейку BeginArrowSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровлине** <br/> |
| Индекс ячейки:  <br/> |**вислинебегинарровсизе** <br/> |
   

