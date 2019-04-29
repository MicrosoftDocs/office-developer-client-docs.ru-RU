---
title: BulletString Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Позволяет создавать пользовательские стили маркеров.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409750"
---
# <a name="bulletstring-cell-paragraph-section"></a>BulletString Cell (Paragraph Section)

Позволяет создавать пользовательские стили маркеров. 
  
## <a name="remarks"></a>Примечания

Введите стиль в виде строки (в кавычках). Например, можно ввести строку "УО".
  
Можно также задать значение этой ячейки, щелкнув фигуру правой кнопкой мыши, выбрав пункт **Формат**, пункт **текст**, а затем выбрав вкладку **маркеры** . 
  
Чтобы получить ссылку на ячейку BulletString по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Para. Буллетстр [ *i* ], где *i* = <1>, 2, 3,...  <br/> |
   
Чтобы получить ссылку на ячейку BulletString по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектионпараграф** <br/> |
|Индекс строки:  <br/> |**висровпараграф** +  *i* , где *i* = 0, 1, 2,...  <br/> |
|Индекс ячейки:  <br/> |**Висбуллетстринг** <br/> |
   

