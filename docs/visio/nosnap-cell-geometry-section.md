---
title: NoSnap Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Определяет, привязываются ли другие фигуры к пути.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408546"
---
# <a name="nosnap-cell-geometry-section"></a>NoSnap Cell (Geometry Section)

Определяет, привязываются ли другие фигуры к пути.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не разрешать привязку других фигур к этому пути.  <br/> |
| FALSE  <br/> | РазРешите другим фигурам привязку к этому пути.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку с функцией Snapin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . Snapin, где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку с параметром Snapin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**Висровкомпонент** <br/> |
| Индекс ячейки:  <br/> |**Вискомпноснап** <br/> |
   

