---
title: Value Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Содержит значение элемента данных фигуры, введенное в диалоговом окне "Определение данных фигуры".
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431906"
---
# <a name="value-cell-shape-data-section"></a>Value Cell (Shape Data Section)

Содержит значение элемента данных фигуры, введенное в диалоговом окне **"Определение данных** фигуры". 
  
## <a name="remarks"></a>Примечания

Формулы, введенные в этой ячейке, переопределяются значениями, которые введены в диалоговом окне **"Определение данных** фигуры". Это верно, даже если для защиты формулы используется функция GUARD. 
  
Чтобы получить ссылку на ячейку Value по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Реквизит.  *Имя*  . Значение, где prop.  *Имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsValue** <br/> |
   

