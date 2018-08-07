---
title: Ячейка LockCalcWH (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Блокирует прямоугольник выделения фигуры, чтобы ее нельзя было обновить при редактировании узел или изменить тип строки в раздел геометрии.
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814119"
---
# <a name="lockcalcwh-cell-protection-section"></a>Ячейка LockCalcWH (раздел "Защита")

Блокирует прямоугольник выделения фигуры, чтобы ее нельзя было обновить при редактировании узел или изменить тип строки в раздел геометрии.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не удалось обновить ширины и высоты.  <br/> |
| FALSE  <br/> | Можно перерасчете ширины и высоты.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockCalcWH  <br/> |
   
Для получения ссылки на ячейки LockCalcWH по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockCalcWH** <br/> |
   

