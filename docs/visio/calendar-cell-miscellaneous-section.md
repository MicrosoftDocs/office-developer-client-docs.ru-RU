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
description: Определяет календарь, который используется, когда Формула ячейки содержит сведения о дате.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337515"
---
# <a name="calendar-cell-miscellaneous-section"></a>Calendar Cell (Miscellaneous Section)

Определяет календарь, который используется, когда Формула ячейки содержит сведения о дате.
  
## <a name="remarks"></a>Комментарии

Возможные значения: 0 (Западный), 1 (арабский Хиджра), 2 (Еврейский лунный), 3 (тайваньский календарь), 4 (японский императоров Реигн), 5 (тайский), 6 (корейский), 7 (на английском языке), 8 (английский), 8 (французский (транслитерация)) и 9 (французский (французский)). 
  
Чтобы получить ссылку на ячейку календаря по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Календарь  <br/> |
   
Чтобы получить ссылку на ячейку календаря по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровмиск** <br/> |
| Индекс ячейки:  <br/> |**Висобжкалендар** <br/> |
   

