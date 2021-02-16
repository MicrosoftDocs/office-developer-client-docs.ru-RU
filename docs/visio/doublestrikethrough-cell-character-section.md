---
title: DoubleStrikethrough Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Определяет, форматирован ли текст в формате двойного загона.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360594"
---
# <a name="doublestrikethrough-cell-character-section"></a>DoubleStrikethrough Cell (Character Section)

Определяет, форматирован ли текст в формате двойного загона.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку DoubleStrikethrough по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char.DoubleStrikethrough[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку DoubleStrikethrough по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter**  +   *i,* *где i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

