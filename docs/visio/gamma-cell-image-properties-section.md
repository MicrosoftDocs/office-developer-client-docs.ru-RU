---
title: Gamma Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Корректирует или корректирует интенсивность изображения для определенного устройства вывода, например монитора или сканера. Значение по умолчанию — 1 (без коррекции).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315206"
---
# <a name="gamma-cell-image-properties-section"></a>Gamma Cell (Image Properties Section)

Корректирует или корректирует интенсивность изображения для определенного устройства вывода, например монитора или сканера. Значение по умолчанию — 1 (без коррекции).
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку гаммы по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ГАММА  <br/> |
   
Чтобы получить ссылку на ячейку гамма по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровимаже** <br/> |
| Индекс ячейки:  <br/> |**Висимажегамма** <br/> |
   

