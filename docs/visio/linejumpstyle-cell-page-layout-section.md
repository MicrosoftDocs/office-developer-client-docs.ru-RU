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
description: Определяет стиль значка пересечения линий для всех соединителей на странице документа, у которых нет стиля значков для локальной линии.
ms.openlocfilehash: 066c96f659061290b825684a479432e6d71f518c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427243"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>LineJumpStyle Cell (Page Layout Section)

Определяет стиль значка пересечения линий для всех соединителей на странице документа, у которых нет стиля значков для локальной линии.
  
|**Значение**|**Стиль значка пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Гипербол  <br/> |**Висложумпстиледефаулт** <br/> |
|1,1  <br/> |Гипербол  <br/> |**Висложумпстилеарк** <br/> |
|2  <br/> |Gap  <br/> |**Висложумпстилегап** <br/> |
|4  <br/> |Го  <br/> |**Висложумпстилескуаре** <br/> |
|SP4  <br/> |2 стороны  <br/> |**Висложумпстилетриангле** <br/> |
|17:00  <br/> |3 стороны  <br/> |**visLOJumpStyle2Point** <br/> |
|ICMPv6  <br/> |4 стороны  <br/> |**visLOJumpStyle3Point** <br/> |
|см  <br/> |5 Сторон  <br/> |**visLOJumpStyle4Point** <br/> |
|8,5  <br/> |6 сторон  <br/> |**visLOJumpStyle5Point** <br/> |
|10  <br/> |7 Сторон  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Примечания

Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).
  
Чтобы получить ссылку на ячейку LineJumpStyle по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineJumpStyle  <br/> |
   
Чтобы получить ссылку на ячейку LineJumpStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровпажелайаут** <br/> |
|Индекс ячейки:  <br/> |**Виспложумпстиле** <br/> |
   

