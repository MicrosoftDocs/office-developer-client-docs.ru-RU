---
title: UIFormat Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Определяет формат вставленного поля в более ранних версиях Visio, чем Visio 2000.
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337144"
---
# <a name="uiformat-cell-text-fields-section"></a>UIFormat Cell (Text Fields Section)

Определяет формат вставленного поля в более ранних версиях Visio, чем Visio 2000.
  
## <a name="remarks"></a>Комментарии

Эта ячейка не отображается в окне таблицы свойств фигуры. Используйте эту ячейку, если вам нужно разобраться с проблемами обратной связи, например сохранить документ Visio версии 2000 в формате файлов Visio версии 5,0.
  
Чтобы получить ссылку на ячейку UIFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields. Уифмт [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку UIFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионтекстфиелд** <br/> |
| Индекс строки:  <br/> |**висровфиелд** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висфиелдуиформат** <br/> |
   

