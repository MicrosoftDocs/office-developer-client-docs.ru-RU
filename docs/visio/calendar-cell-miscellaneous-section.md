---
title: Ячейка Calendar (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Определяет календарь, который будет использоваться при Формула ячейки содержит сведения о дате.
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813312"
---
# <a name="calendar-cell-miscellaneous-section"></a>Ячейка Calendar (раздел "Прочее")

Определяет календарь, который будет использоваться при Формула ячейки содержит сведения о дате.
  
## <a name="remarks"></a>Замечания

Возможные значения: 0 (западное), 1 (арабский хиджра), 2 (Еврейский лунный), 3 (тайваньский), 4 (японский Мэйдзи Reign), 5 (тайский), 6 (корейский Danki), 7 (эра Сака), (транслитерированный английский) 8 и 9 (Транслитерированный французский). 
  
Для получения ссылки на ячейки календаря по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Календарь  <br/> |
   
Для получения ссылки на ячейки календаря по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjCalendar** <br/> |
   

