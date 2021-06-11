---
title: Calendar Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Определяет календарь, используемый для текстового поля, когда тип данных — Дата.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424757"
---
# <a name="calendar-cell-text-fields-section"></a>Calendar Cell (Text Fields Section)

Определяет календарь, используемый для текстового поля, когда тип данных — Дата.
  
## <a name="remarks"></a>Примечания

Возможные значения: 0 (западный), 1 (арабский хиджри), 2 (еврейский лунный), 3 (тайваньский календарь), 4 (японский император Царствование), 5 (тайский буддист), 6 (корейский данки), 7 (сакская эра), 8 (английский транслитерированный) и 9 (французский транслитерированный). 
  
Чтобы получить ссылку на ячейку Calendar по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | *Fields.Calendar[i]* где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Calendar по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTextField** <br/> |
| Индекс строки:  <br/> |**visRowField**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visFieldCalendar** <br/> |
   

