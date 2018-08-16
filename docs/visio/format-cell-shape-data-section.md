---
title: Ячейка Format (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
localization_priority: Normal
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Задает форматирование элемента данных фигуры, — это строка, фиксированный список, число, список переменных, даты или времени, длительность или currency.
ms.openlocfilehash: 48342f21a107ff78fed2347fb679ed8199526056
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813835"
---
# <a name="format-cell-shape-data-section"></a>Ячейка Format (раздел "Данные фигуры")

Задает форматирование элемента данных фигуры, — это строка, фиксированный список, число, список переменных, даты или времени, длительность или currency.
  
## <a name="remarks"></a>Замечания

|**Данные фигуры: тип элемента**|**Значение**|**Формат содержимого ячейки**|
|:-----|:-----|:-----|
| Строка  <br/> | 0  <br/> | Формат рисунка, соответствующий типу данных.  <br/> |
| Фиксированный список  <br/> | 1  <br/> | Элементы, отображаются в списке, разделенных точкой с запятой.  <br/> |
| Number  <br/> | 2  <br/> | Формат рисунка, соответствующий типу данных.  <br/> |
| Список переменных  <br/> | 4  <br/> | Элементы, отображаются в списке, разделенных точкой с запятой.  <br/> |
| Даты или времени  <br/> | 5  <br/> | Формат рисунка, соответствующий типу данных.  <br/> |
| Продолжительность  <br/> | 6  <br/> | Формат рисунка, соответствующий типу данных.  <br/> |
| Денежный  <br/> | 7  <br/> | Формат рисунка, соответствующий типу данных.  <br/> |
   
В качестве примера указания формат рисунка, соответствующий типу данных формат рисунок «# #/ 4 UU» форматов номеров 12.43 in. как 12 2/4 ДЮЙМА. Дополнительные сведения о задании формат рисунка можно [о формате изображений](about-format-pictures.md).
  
Пример указания элементов для списка «Engineering; Отдел кадров; Продажи; Маркетинг».
  
Объект Date values (тип = 5) отображаются в формате краткий формат даты. Денежными значениями (тип = 7) отображаются с помощью параметра текущего пользователя для **валюты** на вкладке **Региональные параметры** в элементе **язык и региональные стандарты** на **Панели управления**.
  
Число (тип = 2) может представлять измерением scalar, угол, даты, времени и денежных единиц. Чтобы убедиться, что ввода номера всегда вычисляется как дата, время или валюты, используйте функцию даты и времени или Квартал в ячейке формат вместо формат рисунка.
  
Для получения ссылки на ячейки формат по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Свойства.  *имя* . Формат где свойств.  *имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки формат по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsFormat** <br/> |
   
