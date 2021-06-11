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
description: Определяет положение текста фигуры по отношению к базовой.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414020"
---
# <a name="pos-cell-character-section"></a>Pos Cell (Character Section)

Определяет положение текста фигуры по отношению к базовой.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Нормальная позиция  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Superscript  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Subscript  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Pos по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char.Pos[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Pos по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterPos** <br/> |
   

