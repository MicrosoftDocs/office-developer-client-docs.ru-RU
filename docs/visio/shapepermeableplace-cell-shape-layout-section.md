---
title: ShapePermeablePlace Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Определяет, можно ли размещать фигуры поверх фигуры при раскладывке фигур в диалоговом окне Настройка макета (на вкладке Дизайн, в группе Макет, щелкните Re-Layout страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427222"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>ShapePermeablePlace Cell (Shape Layout Section)

Определяет, можно ли размещать фигуры поверх фигуры при раскладывке фигур в диалоговом окне **Настройка** макета (на вкладке Дизайн в группе **Макет** щелкните Страницу повторного макета **и** нажмите кнопку Дополнительные параметры  макета). 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включить фигуры, которые должны быть размещены на вершине формы.  <br/> |
|FALSE  <br/> |Не делайте так, чтобы фигуры помещались поверх фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой  ячейки  на вкладке Размещение в диалоговом [](run-in-developer-mode-display-the-developer-tab.md) окне Поведение (с выбранной фигурой на вкладке Разработчик, в группе **Shape Design** нажмите кнопку **Поведение,** а затем щелкните вкладку **Размещение).** 
  
В версиях до Visio 2000 года такое поведение устанавливается с помощью ячейки ObjInteract в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapePermeablePlace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePermeablePlace  <br/> |
   
Чтобы получить ссылку на ячейку ShapePermeablePlace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermeablePlace** <br/> |
   

