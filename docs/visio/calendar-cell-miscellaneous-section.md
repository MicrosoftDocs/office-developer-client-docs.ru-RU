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
description: Определяет календарь, используемый, когда формула ячейки содержит сведения о дате.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421818"
---
# <a name="calendar-cell-miscellaneous-section"></a>Calendar Cell (Miscellaneous Section)

Определяет календарь, используемый, когда формула ячейки содержит сведения о дате.
  
## <a name="remarks"></a>Примечания

Возможные значения: 0 (западный), 1 (арабский хиджри), 2 (еврейский лунный), 3 (тайваньский календарь), 4 (японский император Царствование), 5 (тайский буддист), 6 (корейский данки), 7 (сакская эра), 8 (английский транслитерированный) и 9 (французский транслитерированный). 
  
Чтобы получить ссылку на ячейку Calendar по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Календарь  <br/> |
   
Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjCalendar** <br/> |
   

