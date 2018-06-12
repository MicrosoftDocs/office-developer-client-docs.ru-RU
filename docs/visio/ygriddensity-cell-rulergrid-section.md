---
title: Ячейка YGridDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Указывает тип сетки по вертикали.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815224"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Ячейка YGridDensity (линейки &amp; сетка)

Указывает тип сетки по вертикали.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Предопределенная  <br/> |**visGridFixed** <br/> |
|2  <br/> |Крупной  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Обычный (по умолчанию)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Оптимизация  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует **сетки интервал** по вертикали параметра в **линейки &amp; сетки** диалоговое окно (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку YGridDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |YGridDensity  <br/> |
   
Для получения ссылки на ячейки YGridDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYGridDensity** <br/> |
   

