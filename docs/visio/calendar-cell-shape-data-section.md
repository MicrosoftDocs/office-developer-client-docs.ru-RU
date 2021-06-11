---
title: Calendar Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Определяет календарь, используемый для данных фигуры, когда тип данных — Дата.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432760"
---
# <a name="calendar-cell-shape-data-section"></a>Calendar Cell (Shape Data Section)

Определяет календарь, используемый для данных фигуры, когда тип данных — Дата.
  
## <a name="remarks"></a>Примечания

Возможные значения: 0 (западный), 1 (арабский хиджри), 2 (еврейский лунный), 3 (тайваньский календарь), 4 (японский император Царствование), 5 (тайский буддист), 6 (корейский данки), 7 (сакская эра), 8 (английский транслитерированный) и 9 (французский транслитерированный). 
  
Чтобы получить ссылку на ячейку Calendar по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Prop.  *имя*  . Календарь, в котором prop.  *имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsCalendar** <br/> |
   

