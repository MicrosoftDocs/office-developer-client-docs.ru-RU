---
title: ShapePermeableY Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Определяет, может ли соединитель проходить по вертикали через фигуру.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417520"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>ShapePermeableY Cell (Shape Layout Section)

Определяет, может ли соединитель проходить по вертикали через фигуру.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Позволяет соединителям проходить по вертикали через фигуру.  <br/> |
|FALSE  <br/> |Не позволяйте соединителям проходить по вертикали через фигуру.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой  ячейки  на вкладке "Размещение" в диалоговом окне  "Поведение" (с выбранной фигурой, на вкладке "Разработчик", в группе "Проектирование фигуры" щелкните "Поведение" и выберите вкладку **"Размещение").** [](run-in-developer-mode-display-the-developer-tab.md) 
  
В версиях, более ранних, чем Visio 2000, такое поведение задано с помощью ячейки ObjInteract в разделе "Прочие".
  
Чтобы получить ссылку на ячейку ShapePermeableY по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePermeableY  <br/> |
   
Чтобы получить ссылку на ячейку ShapePermeableY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermY** <br/> |
   

