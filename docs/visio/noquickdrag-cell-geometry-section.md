---
title: NoQuickDrag Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Определяет, можно ли выбрать или перетащить фигуру, когда пользователь щелкает область заливки, определенную в разделе "геометрия".
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341064"
---
# <a name="noquickdrag-cell-geometry-section"></a>NoQuickDrag Cell (Geometry Section)

Определяет, можно ли выбрать или перетащить фигуру, когда пользователь щелкает область заливки, определенную в разделе "геометрия".
  
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку NoQuickDrag по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Геометрия *i* . NoQuickDrag, где * i * – <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку NoQuickDrag по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**виссектионфирсткомпонент** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс строки:  <br/> |**Висровкомпонент** <br/> |
|Индекс ячейки:  <br/> |**Вискомпнокуиккдраг** <br/> |
   

