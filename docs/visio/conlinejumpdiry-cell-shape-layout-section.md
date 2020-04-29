---
title: ConLineJumpDirY Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404773"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>ConLineJumpDirY Cell (Shape Layout Section)

Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
  
|**Значение**|**Направление пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Страница по умолчанию  <br/> |**висложумпдиридефаулт** <br/> |
| 1,1  <br/> | Left  <br/> |**висложумпдирилефт** <br/> |
| 2  <br/> | Right  <br/> |**висложумпдириригхт** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать вертикальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirY в разделе Макет страницы. 
  
Чтобы получить ссылку на ячейку ConLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ConLineJumpDirY  <br/> |
   
Чтобы получить ссылку на ячейку ConLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровшапелайаут** <br/> |
| Индекс ячейки:  <br/> |**виссложумпдири** <br/> |
   

