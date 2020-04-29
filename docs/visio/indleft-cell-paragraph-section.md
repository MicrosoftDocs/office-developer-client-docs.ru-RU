---
title: IndLeft Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Представляет расстояние для всех строк текста в абзаце с отступом от левого поля блока текста. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ слева остается прежним.
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405165"
---
# <a name="indleft-cell-paragraph-section"></a>IndLeft Cell (Paragraph Section)

Представляет расстояние для всех строк текста в абзаце с отступом от левого поля блока текста. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ слева остается прежним.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку IndLeft по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para. IndLeft [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку IndLeft по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**виссектионпараграф** <br/> |
| Индекс строки:  <br/> |**висровпараграф** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**висиндентлефт** <br/> |
   

