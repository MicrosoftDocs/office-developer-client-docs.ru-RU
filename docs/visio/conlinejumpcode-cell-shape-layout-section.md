---
title: ConLineJumpCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Определяет, когда соединители переходов.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421622"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>ConLineJumpCode Cell (Shape Layout Section)

Определяет, когда соединители переходов.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Как указывает страница; На **вкладке "Конструктор"** щелкните стрелку в группе "Настройка страницы", а затем щелкните вкладку  **"Макет** и маршрут", чтобы увидеть спецификации страницы  <br/> |**visSLOJumpDefault** <br/> |
|1   <br/> |Никогда  <br/> |**visSLOJumpNever** <br/> |
|2   <br/> |Постоянно  <br/> |**visSLOJumpAlways** <br/> |
|3   <br/> |Другие переходы соединители  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Ни один из соединители не переходов  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить значение этой ячейки, выбрав динамический  соединитель, щелкнув "Поведение" в группе "Конструктор фигур" на вкладке "Разработчик", а затем выбрав вкладку **"Соединитель".**  [](run-in-developer-mode-display-the-developer-tab.md) 
  
Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ConLineJumpCode  <br/> |
   
Чтобы получить ссылку на ячейку ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOJumpCode** <br/> |
   

