---
title: Ячейка Value (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Содержит функции для поля.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815126"
---
# <a name="value-cell-text-fields-section"></a>Ячейка Value (раздел "Текстовые поля")

Содержит функции для поля.
  
## <a name="remarks"></a>Замечания

Можно задать значение ячейки с помощью диалогового окна **поля** (на вкладке **Вставка** в группе **текст** щелкните **поле**).
  
Чтобы получить ссылку на значение ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Fields.Value [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки значение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionTextField** <br/> |
|Индекс строки:  <br/> |**visRowField** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visFieldCell** <br/> |
   

