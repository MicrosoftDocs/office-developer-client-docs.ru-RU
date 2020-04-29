---
title: Font Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят от установленных в системе шрифтов. Число 0 представляет шрифт по умолчанию, который обычно составляет Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438668"
---
# <a name="font-cell-character-section"></a>Font Cell (Character Section)

Представляет номер шрифта, используемого для форматирования текста. Номера шрифтов зависят от установленных в системе шрифтов. Число 0 представляет шрифт по умолчанию, который обычно составляет Arial.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Font по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char. Font [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Font по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**виссектиончарактер** <br/> |
| Индекс строки:  <br/> |**висровчарактер** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**висчарактерфонт** <br/> |
   

