---
title: Ячейка Pos (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Определяет положение текста фигуры относительно базового плана.
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814468"
---
# <a name="pos-cell-character-section"></a>Ячейка Pos (раздел "Символ")

Определяет положение текста фигуры относительно базового плана.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Обычном положении  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Надстрочный знак  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Подстрочный знак  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку положительные по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Char.Pos [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки положительные по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterPos** <br/> |
   

