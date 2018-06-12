---
title: Ячейка NoQuickDrag (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Определяет, установлен или перетащить при нажатии кнопки Заполненная область, определенные в раздел геометрии фигуры.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814309"
---
# <a name="noquickdrag-cell-geometry-section"></a>Ячейка NoQuickDrag (раздел геометрии)

Определяет, установлен или перетащить при нажатии кнопки Заполненная область, определенные в раздел геометрии фигуры.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoQuickDrag по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Геометрия *i* . NoQuickDrag, где * я * - < 1 >, 2, 3...  <br/> |
   
Для получения ссылки на ячейки NoQuickDrag по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс строки:  <br/> |**visRowComponent** <br/> |
|Индекс ячейки:  <br/> |**visCompNoQuickDrag** <br/> |
   

