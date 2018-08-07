---
title: Ячейка Type / C (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Определяет тип точки подключения.
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815085"
---
# <a name="type--c-cell-connection-points-section"></a>Ячейка Type / C (раздел "Точки соединения")

Определяет тип точки подключения.
  
|**Значение**|**Тип**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Рисунка  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Наружу  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Внутрь &amp; наружу  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать тип точки подключения, Выбор средства **соединителя** , выбрав фигуры и затем щелкните правой кнопкой мыши точку подключения. Для этого необходимо запустить в режиме [разработчика](run-in-developer-mode-display-the-developer-tab.md) . 
  
Для получения ссылки на тип / C ячейка по имени из другой формулы или из файла с помощью свойства **CellsU** использования: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Connections.Type [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на тип / C ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
|Индекс строки:  <br/> |**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visCnnctType** (не только строк) **visCnnctC** (расширенные строк)  <br/> |
   
Сведения о не расширены и расширенного строк, в разделе точек подключения строки.
  

