---
title: Ячейка Value (раздел "Пользовательские ячейки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Задает значение для соответствующей пользовательской ячейки.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815131"
---
# <a name="value-cell-user-defined-cells-section"></a>Ячейка Value (раздел "Пользовательские ячейки")

Задает значение для соответствующей пользовательской ячейки.
  
## <a name="remarks"></a>Замечания

Чтобы указать это значение в ячейке, укажите пользовательских имя, введенное в строке метки User.Row.
  
Чтобы получить ссылку на значение ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Пользователь.  *Имя* . Значение where пользователя.  *Имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки значение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionUser** <br/> |
| Индекс строки:  <br/> |**visRowUser** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visUserValue** <br/> |
   

