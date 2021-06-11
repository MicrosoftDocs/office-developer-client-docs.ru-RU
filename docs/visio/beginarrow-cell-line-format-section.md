---
title: BeginArrow Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Указывает, имеет ли строка наконечник стрелки или другой конечный формат строки на первом вершине. Введите номер от 0 до 45 или функцию USE с именем пользовательского конца строки или используйте диалоговое окно Line.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410296"
---
# <a name="beginarrow-cell-line-format-section"></a>BeginArrow Cell (Line Format Section)

Указывает, имеет ли строка наконечник стрелки или другой конечный формат строки на первом вершине. Введите номер от 0 до 45 или функцию USE с именем пользовательского конца строки или используйте диалоговое окно **Line.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
| 0  <br/> | Без наконечника стрелы.  <br/> |
| 1 - 45  <br/> | Различные стили наконечники стрел, соответствующие индексным записям в диалоговом окне **Line.**  <br/> |
   
## <a name="remarks"></a>Примечания

Размер наконечник стрелки устанавливается в ячейке BeginArrowSize.
  
Чтобы получить ссылку на ячейку BeginArrow по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BeginArrow  <br/> |
   
Чтобы получить ссылку на ячейку BeginArrow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLine** <br/> |
| Индекс ячейки:  <br/> |**visLineBeginArrow** <br/> |
   

