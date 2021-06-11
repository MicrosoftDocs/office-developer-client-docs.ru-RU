---
title: ShdwType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Указывает тип теней по умолчанию для страницы.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424100"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType Cell (Page Properties Section)

Указывает тип теней по умолчанию для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 1  <br/> | Простой  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Косая  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Внутренняя  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Примечания

 Тип теней, описанный в этой ячейке, используется всякий раз, когда ячейка ShapeShdwType (тип теней для отдельной фигуры на странице) задает значение Page Default **(visFSTPageDefault).** 
  
Простые типы теней описываются как офсетные тени в пользовательском интерфейсе (пользовательском интерфейсе). Простая тень дает эффект от затеняемой фигуры на параллельном плоскости, расположенном на некотором расстоянии за ней. Косые тени описываются как косые тени в пользовательском интерфейсе и дают эффект отбрасываемой тени на плоскость перпендикулярно фигуре. 
  
Список предопределяемого простого и косого теневого типа см. в  списке Style на вкладке **Shadows** диалогового окна Установки страницы (на вкладке **Design** нажмите стрелку установки страницы).   
  
Чтобы получить ссылку на ячейку ShdwType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwType  <br/> |
   
Чтобы получить ссылку на ячейку ShapeShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwType** <br/> |
   

