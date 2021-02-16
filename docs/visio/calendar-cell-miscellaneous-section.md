---
title: Calendar Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Определяет календарь, который используется, когда формула ячейки содержит сведения о дате.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421818"
---
# <a name="calendar-cell-miscellaneous-section"></a>Calendar Cell (Miscellaneous Section)

Определяет календарь, который используется, когда формула ячейки содержит сведения о дате.
  
## <a name="remarks"></a>Примечания

Возможные значения: 0 (западное), 1 (арабский Хиджра), 2 (иврит, иврит, Иврит), 3 (тайваньский календарь), 4 (японский посвещенный по-японски), 5 (тайский посказок), 6 (корейский Данки), 7 (Saka Era), 8 (транслитерированный английский язык) и 9 (перелитерированный французский). 
  
Чтобы получить ссылку на ячейку Календаря по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Календарь  <br/> |
   
Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjCalendar** <br/> |
   

