---
title: Ячейка LockHeight (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Блокирует высоту фигуры таким образом, чтобы его высота не изменяется при изменении размера фигуры.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814137"
---
# <a name="lockheight-cell-protection-section"></a>Ячейка LockHeight (раздел "Защита")

Блокирует высоту фигуры таким образом, чтобы его высота не изменяется при изменении размера фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Высота блокировки.  <br/> |
| FALSE  <br/> | Высота не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockHeight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockHeight  <br/> |
   
Для получения ссылки на ячейки LockHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockHeight** <br/> |
   

