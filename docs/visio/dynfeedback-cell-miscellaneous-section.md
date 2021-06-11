---
title: DynFeedback Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Изменяет тип визуальной обратной связи, предоставляемой пользователям при перетаскивания соединитетеля. Когда кнопка мыши будет выпущена, на фигуру соединитетеля не влияет этот параметр. Этот параметр не применяется к соединитетелям маршрутивируемых маршрутов.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404801"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>DynFeedback Cell (Miscellaneous Section)

Изменяет тип визуальной обратной связи, предоставляемой пользователям при перетаскивания соединитетеля. Когда кнопка мыши будет выпущена, на фигуру соединитетеля не влияет этот параметр. Этот параметр не применяется к соединитетелям маршрутивируемых маршрутов.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Остается прямым (без ног).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Показывает три ноги при перетаскивание.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Показывает пять ног при перетаскивание.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку DynFeedback по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DynFeedback  <br/> |
   
Чтобы получить ссылку на ячейку DynFeedback по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visDynFeedback** <br/> |
   

