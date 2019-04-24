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
description: Определяет, может ли соединитель маршрутизироваться вертикально через фигуру.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326518"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>ShapePermeableY Cell (Shape Layout Section)

Определяет, может ли соединитель маршрутизироваться вертикально через фигуру.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |РазРешите соединители вертикально маршрутизировать через фигуру.  <br/> |
|FALSE  <br/> |Соединители не могут маршрутизироваться вертикально через фигуру.  <br/> |
   
## <a name="remarks"></a>Замечания

Вы также можете задать значение этой ячейки на вкладке " **Размещение** " в диалоговом окне **поведение** (с выбранной фигурой на вкладке " [разработчик](run-in-developer-mode-display-the-developer-tab.md) ", в группе " **Макет фигуры** " щелкните **поведение**, а затем перейдите на вкладку **Размещение** . ). 
  
В версиях, предшествующих Visio 2000, это поведение задается с помощью ячейки Обжинтеракт в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapePermeableY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePermeableY  <br/> |
   
Чтобы получить ссылку на ячейку ShapePermeableY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровшапелайаут** <br/> |
|Индекс ячейки:  <br/> |**Висслоперми** <br/> |
   

