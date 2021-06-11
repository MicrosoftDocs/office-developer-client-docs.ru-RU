---
title: LineJumpStyle Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Определяет стиль перехода строки для всех соединители на странице рисования, которые не имеют локального стиля перехода строки.
ms.openlocfilehash: 066c96f659061290b825684a479432e6d71f518c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427243"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>LineJumpStyle Cell (Page Layout Section)

Определяет стиль перехода строки для всех соединители на странице рисования, которые не имеют локального стиля перехода строки.
  
|**Значение**|**Стиль перехода строки**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Arc  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |2 стороны  <br/> |**visLOJumpStyleTriangle** <br/> |
|5   <br/> |3 стороны  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 стороны  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 сторон  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 сторон  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 сторон  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineJumpStyle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineJumpStyle  <br/> |
   
Чтобы получить ссылку на ячейку LineJumpStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpStyle** <br/> |
   

