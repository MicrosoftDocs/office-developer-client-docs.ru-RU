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
| 1   <br/> | Простой  <br/> |**visFSTSimple** <br/> |
| 2   <br/> | Oblique  <br/> |**visFSTOblique** <br/> |
|3   <br/> |Внутренний  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Примечания

 Тип теней, описанный в этой ячейке, используется, когда для ячейки ShapeShdwType (тип теней для отдельной фигуры на странице) установлено значение Page Default (**visFSTPageDefault).** 
  
Простые типы теней описываются как тени смещения в пользовательском интерфейсе. Простая тень дает эффект тени фигуры на параллельную плоскость, расположенную на некотором расстоянии от нее. Косые тени описываются как косые тени в пользовательском интерфейсе и дают эффект отвершения тени на плоскость, перпендикулярную фигуре. 
  
Список предопределяемых простых и нестрогих  типов теней  см. в  списке стилей на  вкладке "Тени" диалоговых окна "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку "Настройка страницы").  
  
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
   

