---
title: PageLineJumpDirX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Определяет направление прыжков строки на горизонтальных динамических соединители на странице рисования, для которой не применено локальное направление прыжка.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431010"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>PageLineJumpDirX Cell (Page Layout Section)

Определяет направление прыжков строки на горизонтальных динамических соединители на странице рисования, для которой не применено локальное направление прыжка.
  
|**Значение**|**Направление перехода строки**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; слева или параметр страницы для фигур  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Up  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Down  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLineJumpDirX  <br/> |
   
Чтобы получить ссылку на ячейку PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOJumpDirX** <br/> |
   

