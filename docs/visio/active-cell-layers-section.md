---
title: Active Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Указывает, активен ли слой. Фигуры без заранее назначенного уровня назначены активному слою(ы), когда вы перетаскивать их на страницу рисования.
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417436"
---
# <a name="active-cell-layers-section"></a>Active Cell (Layers Section)

Указывает, активен ли слой. Фигуры без заранее назначенного уровня назначены активному слою(ы), когда вы перетаскивать их на страницу рисования.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Слой активен.  <br/> |
|FALSE  <br/> |Слой не активен.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение в этой ячейке соответствует параметру **Active** в диалоговом  окне **Layer Properties** (в группе редактирования на вкладке **Home** щелкните Слои **и** нажмите кнопку Свойства **слоя).**
  
Чтобы получить ссылку на активную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Active[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на активную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visLayerActive** <br/> |
   

