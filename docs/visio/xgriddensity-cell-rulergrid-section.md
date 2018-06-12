---
title: Ячейка XGridDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Указывает тип сетки по горизонтали.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815194"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Ячейка XGridDensity (линейки &amp; сетка)

Указывает тип сетки по горизонтали.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Предопределенная  <br/> |**visGridFixed** <br/> |
|2  <br/> |Крупной  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Обычный (по умолчанию)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Оптимизация  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует горизонтальный **Интервал сетки** параметра в **линейки &amp; сетки** диалоговое окно (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |XGridDensity  <br/> |
   
Для получения ссылки на ячейки XGridDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridDensity** <br/> |
   

