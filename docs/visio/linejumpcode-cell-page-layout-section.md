---
title: LineJumpCode Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Определяет соединители, к которым необходимо добавить прыжки.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416253"
---
# <a name="linejumpcode-cell-page-layout-section"></a>LineJumpCode Cell (Page Layout Section)

Определяет соединители, к которым необходимо добавить прыжки.
  
|**Значение**|**Соединители, к которым необходимо добавить прыжки**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Нет  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Горизонтальные линии  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Вертикальные линии  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Последняя маршрутная строка  <br/> |**visPLOJumpLastRouted** <br/> |
|4   <br/> |Последняя отображаемая строка  (верхняя фигура в z-order)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5   <br/> |Первая отображаемая строка (форма  в нижней части z-order)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).
  
Чтобы получить ссылку на ячейку LineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LineJumpCode  <br/> |
   
Чтобы получить ссылку на ячейку LineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOJumpCode** <br/> |
   

