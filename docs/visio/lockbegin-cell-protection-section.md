---
title: Ячейка LockBegin (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Блокирует начальную точку (НачалоX, НачалоY) одномерной фигуры в определенное расположение.
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814113"
---
# <a name="lockbegin-cell-protection-section"></a>Ячейка LockBegin (раздел "Защита")

Блокирует начальную точку (НачалоX, НачалоY) одномерной фигуры в определенное расположение.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Заблокированный начальной точки.  <br/> |
| FALSE  <br/> | Начните не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockBegin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockBegin  <br/> |
   
Для получения ссылки на ячейки LockBegin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockBegin** <br/> |
   

