---
title: Ячейка LockFormat (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Блокирует форматирование фигуры, поэтому его нельзя изменить.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814130"
---
# <a name="lockformat-cell-protection-section"></a>Ячейка LockFormat (раздел "Защита")

Блокирует форматирование фигуры, поэтому его нельзя изменить.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Форматирование нельзя изменить.  <br/> |
| FALSE  <br/> | Форматирование можно изменить.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockFormat  <br/> |
   
Для получения ссылки на ячейки LockFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockFormat** <br/> |
   

