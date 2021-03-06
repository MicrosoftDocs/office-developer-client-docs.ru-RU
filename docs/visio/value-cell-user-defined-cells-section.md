---
title: Value Cell (User-Defined Cells Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Указывает значение для соответствующей ячейки, определенной пользователем.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422992"
---
# <a name="value-cell-user-defined-cells-section"></a>Value Cell (User-Defined Cells Section)

Указывает значение для соответствующей ячейки, определенной пользователем.
  
## <a name="remarks"></a>Примечания

Чтобы сослаться на это значение в другой ячейке, укажите имя, определенное пользователем, вписалось в строковую метку User.Row.
  
Чтобы получить ссылку на ячейку Value по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Пользователь.  *Имя*  . Значение, в котором пользователь.  *Имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionUser** <br/> |
| Индекс строки:  <br/> |**visRowUser**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visUserValue** <br/> |
   

