---
title: Type / C Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Определяет тип точки подключения.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415238"
---
# <a name="type--c-cell-connection-points-section"></a>Type / C Cell (Connection Points Section)

Определяет тип точки подключения.
  
|**Значение**|**Тип**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Входящего  <br/> |**вискннкттипеинвард** <br/> |
|1,1  <br/> |Наруж  <br/> |**вискннкттипеаутвард** <br/> |
|2  <br/> |&amp; Внешнее  <br/> |**вискннкттипеинвардаутвард** <br/> |
   
## <a name="remarks"></a>Примечания

Кроме того, можно задать тип точки подключения, выбрав инструмент **соединитель** , выбрав фигуру и щелкнув правой кнопкой мыши точку подключения. Для этого необходимо запустить в режиме [разработчика](run-in-developer-mode-display-the-developer-tab.md) . 
  
Чтобы получить ссылку на ячейку Type/C по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Connections. Type [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Type/C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
|Индекс строки:  <br/> |**висровконнектионптс** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**вискннкттипе** (нерасширенные строки) **вискннктк** (расширенные строки)  <br/> |
   
Сведения о нерасширенных и расширенных строках можно найти в статье точки подключения.
  

