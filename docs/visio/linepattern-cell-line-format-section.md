---
title: LinePattern Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Определяет шаблон линии фигуры. Значение, введенного в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416757"
---
# <a name="linepattern-cell-line-format-section"></a>LinePattern Cell (Line Format Section)

Определяет шаблон линии фигуры. Значение, введенного в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Без шаблона строки  <br/> |
|1   <br/> |Сплошная  <br/> |
|2 - 23  <br/> |Различные шаблоны строк  <br/> |
   
## <a name="remarks"></a>Примечания

Вы можете просмотреть коллекцию шаблонов линий в  диалоговом  окне **"Линия"** (на вкладке "Главная" в группе "Фигура" щелкните **"Линия",**"На пунктиры" и "Дополнительные **строки").**
  
Чтобы указать пользовательский шаблон строки, используйте функцию USE в этой ячейке.
  
Чтобы получить ссылку на ячейку LinePattern по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LinePattern  <br/> |
   
Чтобы получить ссылку на ячейку LinePattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLine** <br/> |
|Индекс ячейки:  <br/> |**visLinePattern** <br/> |
   

