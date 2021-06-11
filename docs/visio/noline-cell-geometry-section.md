---
title: NoLine Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Определяет, нарисована ли строка вокруг границы пути.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433754"
---
# <a name="noline-cell-geometry-section"></a>NoLine Cell (Geometry Section)

Определяет, нарисована ли строка вокруг границы пути.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Линия не нарисована вокруг границы пути, которая является границей заполненного региона.  <br/> |
| FALSE  <br/> | Линия нарисована вокруг границы пути.  <br/> |
   
## <a name="remarks"></a>Примечания

При изменении цвета строки на белый она по-прежнему существует, даже если ее не видно на белом фоне. При заданной значении этой ячейки значение TRUE не будет ни одной строки.
  
Чтобы получить ссылку на ячейку NoLine по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия  *i*  . NoLine, где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку NoLine по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoLine** <br/> |
   

