---
title: Overline Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Определяет, содержит ли текст линию над ним.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327050"
---
# <a name="overline-cell-character-section"></a>Overline Cell (Character Section)

Определяет, содержит ли текст линию над ним.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Над текстом есть линия.  <br/> |
|FALSE  <br/> |Текст не содержит линию.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этой ячейки также можно задать с помощью диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ). 
  
Чтобы получить ссылку на ячейку "строка" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char. перечеркивание [ *i* ], где *i* = <1>, 2. 3...  <br/> |
   
Чтобы получить ссылку на ячейку с подчеркиванием по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектиончарактер** <br/> |
|Индекс строки:  <br/> |**висровчарактер** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**Висчарактероверлине** <br/> |
   

