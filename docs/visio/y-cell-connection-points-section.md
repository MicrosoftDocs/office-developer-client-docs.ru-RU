---
title: Ячейка Y (раздел указывает подключение)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Представляет y-координаты точки подключения в локальной системе координат.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815196"
---
# <a name="y-cell-connection-points-section"></a>Ячейка Y (раздел указывает подключение)

Представляет *y* -координаты точки подключения в локальной системе координат. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Y по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Connections.Y *i* где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
| Индекс строки:  <br/> |**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visY** <br/> |
   

