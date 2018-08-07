---
title: Ячейка Position (раздел "Вкладки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Задает позиции табуляции. Положение вкладки не зависит от масштаба документа. Если документа изменяется, положение вкладки не изменится.
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814481"
---
# <a name="position-cell-tabs-section"></a>Ячейка Position (раздел "Вкладки")

Задает позиции табуляции. Положение вкладки не зависит от масштаба документа. Если документа изменяется, положение вкладки не изменится.
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки положение по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Вкладки.  *ij* где *i* и *j* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки положение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTab** <br/> |
| Индекс строки:  <br/> |**visRowTab** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j* * 3) + **visTabPos** <br/> |
   

