---
title: Ячейка LockSelect (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Запрещает выбранной фигуры.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814157"
---
# <a name="lockselect-cell-protection-section"></a>Ячейка LockSelect (раздел Защита)

Запрещает выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Невозможно выбрать фигуры.  <br/> |
| FALSE  <br/> | Можно выбирать фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы LockSelect вступили в силу необходимо выбрать флажок **фигур** в диалоговом окне **Защита документа** . 
  
Чтобы получить ссылку на ячейку LockSelect по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockSelect  <br/> |
   
Для получения ссылки на ячейки LockSelect по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockSelect** <br/> |
   

