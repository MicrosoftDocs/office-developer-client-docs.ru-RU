---
title: Ячейка D (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Вспомогательной ячеек, которые можно использовать для ввода и проверки формул.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813527"
---
# <a name="d-cell-connection-points-section"></a>Ячейка D (раздел "Точки соединения")

Вспомогательной ячеек, которые можно использовать для ввода и проверки формул.
  
## <a name="remarks"></a>Замечания

Для доступа к ячейке D, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню. 
  
Чтобы получить ссылку на ячейке D по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Connections.D [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки D по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
| Индекс строки:  <br/> |**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCnnctD** <br/> |
   

