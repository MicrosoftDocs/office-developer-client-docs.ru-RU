---
title: Size Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Определяет размер текста в блоке текста фигуры.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415602"
---
# <a name="size-cell-character-section"></a>Size Cell (Character Section)

Определяет размер текста в блоке текста фигуры.
  
## <a name="remarks"></a>Примечания

Размер текста не зависит от масштаба рисунка. Если масштаб документа изменяется, размер текста остается прежним.
  
Чтобы получить ссылку на ячейку size по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char. size [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку size по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектиончарактер** <br/> |
| Индекс строки:  <br/> |**висровчарактер** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висчарактерсизе** <br/> |
   

