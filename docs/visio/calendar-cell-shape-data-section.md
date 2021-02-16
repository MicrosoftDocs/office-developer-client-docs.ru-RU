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
description: Определяет календарь, используемый для данных фигуры, когда типом данных является Date.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432760"
---
# <a name="calendar-cell-shape-data-section"></a>Calendar Cell (Shape Data Section)

Определяет календарь, используемый для данных фигуры, когда типом данных является Date.
  
## <a name="remarks"></a>Примечания

Возможные значения: 0 (западное), 1 (арабский Хиджра), 2 (иврит, иврит, Иврит), 3 (тайваньский календарь), 4 (японский посвещенный по-японски), 5 (тайский посказок), 6 (корейский Данки), 7 (Saka Era), 8 (транслитерированный английский язык) и 9 (перелитерированный французский). 
  
Чтобы получить ссылку на ячейку Календаря по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Реквизит.  *name*  . Календарь, в котором есть реквизит.  *name*  — имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsCalendar** <br/> |
   

