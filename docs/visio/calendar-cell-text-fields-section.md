---
title: Ячейка Calendar (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Определяет календарь, который используется для текстового поля, когда тип данных даты.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813302"
---
# <a name="calendar-cell-text-fields-section"></a>Ячейка Calendar (раздел "Текстовые поля")

Определяет календарь, который используется для текстового поля, когда тип данных даты.
  
## <a name="remarks"></a>Замечания

Возможные значения: 0 (западное), 1 (арабский хиджра), 2 (Еврейский лунный), 3 (тайваньский), 4 (японский Мэйдзи Reign), 5 (тайский), 6 (корейский Danki), 7 (эра Сака), (транслитерированный английский) 8 и 9 (Транслитерированный французский). 
  
Для получения ссылки на ячейки календаря по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Fields.Calendar [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки календаря по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visFieldCalendar** <br/> |
   

