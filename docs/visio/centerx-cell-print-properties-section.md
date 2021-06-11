---
title: CenterX Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Определяет, по центру ли страница рисования горизонтально на странице принтера.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418080"
---
# <a name="centerx-cell-print-properties-section"></a>CenterX Cell (Print Properties Section)

Определяет, по центру ли страница рисования горизонтально на странице принтера. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Центр страницы рисования горизонтально на странице принтера.  <br/> |
| FALSE  <br/> | Не центрить страницу рисования горизонтально на странице принтера (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

По умолчанию страницы рисования оправданы в верхней и левой части страницы принтера. Настройка ячеек CenterX и CenterY в TRUE помещает страницу рисования в центре страницы принтера (или страниц, когда это необходимо). 
  
Чтобы получить ссылку на ячейку CenterX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | CenterX  <br/> |
   
Чтобы получить ссылку на ячейку CenterX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

