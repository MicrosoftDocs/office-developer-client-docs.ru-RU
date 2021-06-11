---
title: DropOnPageScale Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423764"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>DropOnPageScale Cell (Miscellaneous Section)

Содержит процент масштабирования фигуры при сброшении на страницу рисования.
  
## <a name="remarks"></a>Примечания

В следующих двух случаях Visio масштабировать фигуры таким образом, чтобы они надлежащим образом появлялись на странице рисования:
  
- Если неизмеряемые фигуры сброшены на масштабные рисунки.
    
- Когда измеренные фигуры сброшены на немасштабные рисунки.
    
Процент в ячейке DropOnPageScale указывает на фактор, с помощью которого Visio масштабировать фигуру вверх \> (100) или вниз \< (100). Этот номер можно использовать в качестве фактора при вычислении значений с жесткой кодией. 
  
Это значение составляет 100% для измеренных фигур на масштабных рисунках или необмерных фигур на немасштабных рисунках. 
  
Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DropOnPageScale  <br/> |
   
Чтобы получить ссылку на ячейку DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjDropOnPageScale** <br/> |
   

