---
title: CenterY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Определяет, находится ли страница рисования по центру вертикально на странице принтера.
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437436"
---
# <a name="centery-cell-print-properties-section"></a>CenterY Cell (Print Properties Section)

Определяет, находится ли страница рисования по центру вертикально на странице принтера. 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | По центру страницы рисования вертикально на странице принтера.  <br/> |
| FALSE  <br/> | Не нарисуем страницу рисования по вертикали на странице принтера (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

По умолчанию страницы рисования имеют верхней и левой части страницы принтера. При установке для ячеек CenterX и CenterY в true страница рисования помещается в центр страницы принтера (или страницы, когда требуется установка плитки). 
  
Чтобы получить ссылку на ячейку CenterY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | CenterY  <br/> |
   
Чтобы получить ссылку на ячейку CenterY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPrintProperties** <br/> |
| Индекс ячейки:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

