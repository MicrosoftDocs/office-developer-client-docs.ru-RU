---
title: Ячейка DropOnPageScale (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813649"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Ячейка DropOnPageScale (раздел "Прочее")

Содержит процентную долю, с помощью которого масштабирования фигуры при удаленной на странице документа.
  
## <a name="remarks"></a>Замечания

В следующих двух случаях Visio масштабов фигур, чтобы они отображаются должным образом на странице документа:
  
- При перетаскивании Ненормированный фигур в масштабируемого документы.
    
- При перетаскивании измеренное фигур в зависимым документы.
    
Процент в ячейке DropOnPageScale указывает коэффициент, с помощью которого Visio масштабируемая фигуры, либо копирование (\>100) или вниз (\<100). Можно использовать этот номер как коэффициент при расчете фиксированными значениями. 
  
Это значение равно 100% для измеренное фигур на масштабируемого документы или Ненормированный фигур на зависимым документы. 
  
Чтобы получить ссылку на ячейку DropOnPageScale по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DropOnPageScale  <br/> |
   
Для получения ссылки на ячейки DropOnPageScale по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjDropOnPageScale** <br/> |
   
