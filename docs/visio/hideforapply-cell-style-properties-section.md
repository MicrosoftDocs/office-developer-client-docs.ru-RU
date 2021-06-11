---
title: HideForApply Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Определяет, где в пользовательском интерфейсе Microsoft Visio показан стиль.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423246"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply Cell (Style Properties Section)

Определяет, где в пользовательском интерфейсе Microsoft Visio показан стиль.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Покажите стиль только в **обозревателе рисования.**  <br/> |
| FALSE  <br/> | Показать стиль в **обозревателе рисования**.  <br/> |
   
## <a name="remarks"></a>Примечания

При основании нового стиля на скрытый стиль новый стиль не наследует этот атрибут.
  
Чтобы получить ссылку на ячейку HideForApply по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | HideForApply  <br/> |
   
Чтобы получить ссылку на ячейку HideForApply по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowStyle** <br/> |
| Индекс ячейки:  <br/> |**visStyleHidden** <br/> |
   

