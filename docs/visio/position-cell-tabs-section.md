---
title: Position Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Указывает позицию табуляции. Позиция табуляции не зависит от масштаба документа. Если масштаб документа изменяется, положение вкладки остается прежним.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307751"
---
# <a name="position-cell-tabs-section"></a>Position Cell (Tabs Section)

Указывает позицию табуляции. Позиция табуляции не зависит от масштаба документа. Если масштаб документа изменяется, положение вкладки остается прежним.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Position по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Знаков.  *ИЖ* , где *i* и *j* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Position по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионтаб** <br/> |
| Индекс строки:  <br/> |**висровтаб** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j* * 3) + **вистабпос** <br/> |
   

