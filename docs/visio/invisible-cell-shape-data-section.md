---
title: Invisible Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Указывает, виден ли элемент данных фигуры в окне "Данные фигуры".
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405319"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible Cell (Shape Data Section)

Указывает, виден ли элемент данных фигуры в **окне "Данные** фигуры". 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Элемент данных фигуры не виден.  <br/> |
| FALSE  <br/> | Элемент данных фигуры виден.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение в этой ячейке  соответствует скрытому  окну в диалоговом окне "Определение данных фигуры" (щелкните правой кнопкой мыши фигуру, найдите пункт **"Данные"** и выберите пункт **"Определить данные фигуры").**
  
Чтобы получить ссылку на ячейку Invisible по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Реквизит.  *name*  . Невидимый, где реквизит.  *name*  — имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Invisible по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsInvis** <br/> |
   

