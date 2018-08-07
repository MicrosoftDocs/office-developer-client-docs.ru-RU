---
title: Ячейка NoSnap (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Определяет, привязываются ли другие элементы к пути.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814310"
---
# <a name="nosnap-cell-geometry-section"></a>Ячейка NoSnap (раздел "Геометрия")

Определяет, привязываются ли другие элементы к пути.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не разрешать другие фигуры, чтобы привязать к этому пути.  <br/> |
| FALSE  <br/> | Разрешить другие фигуры, чтобы привязать к этому пути.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoSnap по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . NoSnap где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки NoSnap по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoSnap** <br/> |
   

