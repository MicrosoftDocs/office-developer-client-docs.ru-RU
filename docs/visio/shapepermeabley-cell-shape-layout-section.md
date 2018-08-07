---
title: Ячейка ShapePermeableY (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Определяет ли соединитель могут перенаправлять вертикально через фигуру.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814769"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Ячейка ShapePermeableY (раздел "Макет фигуры")

Определяет ли соединитель могут перенаправлять вертикально через фигуру.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включение соединителей для маршрутизации вертикально через фигуру.  <br/> |
|FALSE  <br/> |Нельзя допускать маршрут соединители вертикально через фигуру.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ). 
  
В версии более ранней, чем Visio 2000 устанавливаются это поведение с помощью ObjInteract ячейки в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapePermeableY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapePermeableY  <br/> |
   
Для получения ссылки на ячейки ShapePermeableY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermY** <br/> |
   

