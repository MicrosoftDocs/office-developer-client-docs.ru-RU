---
title: NoFill Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Указывает, можно ли заполнить путь.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357255"
---
# <a name="nofill-cell-geometry-section"></a>NoFill Cell (Geometry Section)

Указывает, можно ли заполнить путь.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Путь не заполняется, даже если другие пути в фигуре заполнены.  <br/> |
| FALSE  <br/> | Заливка фигуры применяется к пути, даже если она не закрыта.  <br/> |
   
## <a name="remarks"></a>Примечания

Если для узора заливки фигуры задано значение None (0), ни один из его путей не заполняется. Эта ячейка используется для того, чтобы отключить выборочную заливку для контура в фигуре.
  
Чтобы получить ссылку на ячейку "FILLIN" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . Замещение, где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку "FILLIN" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**Висровкомпонент** <br/> |
| Индекс ячейки:  <br/> |**Вискомпнофилл** <br/> |
   

