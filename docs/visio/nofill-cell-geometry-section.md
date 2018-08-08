---
title: Ячейка NoFill (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Указывает, можно ли заполнить путь.
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814300"
---
# <a name="nofill-cell-geometry-section"></a>Ячейка NoFill (раздел "Геометрия")

Указывает, можно ли заполнить путь.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Путь не указана, даже в том случае, если заполняются других путей к папкам в форме.  <br/> |
| FALSE  <br/> | Заливки фигуры применяется к пути, даже в том случае, если оно не будет закрыто.  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение none (0) значение узора заливки фигуры, ни один из его пути не будут заполнены. В этой ячейке используется для отключить заливки выборочно для пути внутри фигуры.
  
Чтобы получить ссылку на ячейку NoFill по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . NoFill где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки NoFill по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoFill** <br/> |
   

