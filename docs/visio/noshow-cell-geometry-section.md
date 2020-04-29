---
title: NoShow Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Указывает, отображается ли путь на странице документа.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410352"
---
# <a name="noshow-cell-geometry-section"></a>NoShow Cell (Geometry Section)

Указывает, отображается ли путь на странице документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Обводка и заливка контура, представленного в разделе, скрыта.  <br/> |
| FALSE  <br/> | Отображается обводка и заливка контура.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Show по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . Показать, где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Show по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**висровкомпонент** <br/> |
| Индекс ячейки:  <br/> |**вискомпношов** <br/> |
   

