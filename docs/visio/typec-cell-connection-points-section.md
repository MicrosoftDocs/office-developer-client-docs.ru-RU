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
|0  <br/> |Внутреннее  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Внешний  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Внутреннее &amp; внешнее  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить тип точки подключения, выбрав средство **Connector,** выбрав фигуру, а затем щелкнув правой кнопкой мыши точку подключения. Для этого необходимо запустить в режиме [разработчика.](run-in-developer-mode-display-the-developer-tab.md) 
  
Чтобы получить ссылку на ячейку Type /C по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Connections.Type[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Type /C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
|Индекс строки:  <br/> |**visRowConnectionPts**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCnnctType** (не расширенные строки) **visCnnctC** (расширенные строки)  <br/> |
   
Сведения о расширенных и расширенных строках см. в строке Точки подключения.
  

