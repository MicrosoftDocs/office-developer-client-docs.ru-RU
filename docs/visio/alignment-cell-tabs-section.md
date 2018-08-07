---
title: Ячейка Alignment (раздел "Вкладки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Задает выравнивание табуляции.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813139"
---
# <a name="alignment-cell-tabs-section"></a>Ячейка Alignment (раздел "Вкладки")

Задает выравнивание табуляции.
  
|**Значение**|**Выравнивание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Center  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Right  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Decimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Разделители  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки выравнивание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Вкладки.  *ij* где *i и j =* < 1 > 2, 3  <br/> |
   
Для получения ссылки на ячейки выравнивание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTab** <br/> |
| Индекс строки:  <br/> |**visRowTab +** *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

