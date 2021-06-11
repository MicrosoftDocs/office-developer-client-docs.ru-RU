---
title: Alignment Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Указывает выравнивание вкладок.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425542"
---
# <a name="alignment-cell-tabs-section"></a>Alignment Cell (Tabs Section)

Указывает выравнивание вкладок.
  
|**Значение**|**Alignment**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Center  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Right  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Десятичное число  <br/> |**visTabStopDecimal** <br/> |
| 4   <br/> | Запятая  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Выравнивание по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Вкладки.  *ij,*            *где i и j =*  <1>, 2, 3  <br/> |
   
Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTab** <br/> |
| Индекс строки:  <br/> |**visRowTab +** *i,*            *где i*  = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j*  *3) **+ visTabAlign** <br/> |
   

