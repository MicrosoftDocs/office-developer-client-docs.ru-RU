---
title: Pos Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Определяет положение текста фигуры относительно базового плана.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359817"
---
# <a name="pos-cell-character-section"></a>Pos Cell (Character Section)

Определяет положение текста фигуры относительно базового плана.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Обычное положение  <br/> |**Виспоснормал** <br/> |
| 1,1  <br/> | Superscript  <br/> |**Виспоссупер** <br/> |
| 2  <br/> | Subscript  <br/> |**Виспоссуб** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку POS по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char. POS [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку POS по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектиончарактер** <br/> |
| Индекс строки:  <br/> |**висровчарактер** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висчарактерпос** <br/> |
   

