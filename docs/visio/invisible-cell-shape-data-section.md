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
description: Указывает, виден ли элемент данных фигуры в окне Shape Data.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405319"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible Cell (Shape Data Section)

Указывает, виден ли элемент данных фигуры в **окне Shape Data.** 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Элемент фигуры данных не виден.  <br/> |
| FALSE  <br/> | Видна фигура элемента данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение в этой ячейке  соответствует скрытому чековом окну в диалоговом окне **Define Shape Data** (щелкните правой кнопкой мыши фигуру, указать на **данные,** а затем нажмите кнопку **Определить данные фигуры).**
  
Чтобы получить ссылку на невидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Prop.  *имя*  . Невидимый, где Prop.  *имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на невидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsInvis** <br/> |
   

