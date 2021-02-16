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
description: Представляет число шрифта, используемого для формата текста. Номера шрифтов зависят от шрифтов, установленных в системе. Число 0 представляет шрифт по умолчанию, который обычно является Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438668"
---
# <a name="font-cell-character-section"></a>Font Cell (Character Section)

Представляет число шрифта, используемого для формата текста. Номера шрифтов зависят от шрифтов, установленных в системе. Число 0 представляет шрифт по умолчанию, который обычно является Arial.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Font по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Char.Font[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Font по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionCharacter** <br/> |
| Индекс строки:  <br/> |**visRowCharacter**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCharacterFont** <br/> |
   

