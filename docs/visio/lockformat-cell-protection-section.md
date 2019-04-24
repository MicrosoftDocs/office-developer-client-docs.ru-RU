---
title: LockFormat Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Блокирует форматирование фигуры, чтобы его нельзя было изменить.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359615"
---
# <a name="lockformat-cell-protection-section"></a>LockFormat Cell (Protection Section)

Блокирует форматирование фигуры, чтобы его нельзя было изменить.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Форматирование не может быть изменено.  <br/> |
| FALSE  <br/> | Форматирование можно изменить.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockFormat  <br/> |
   
Чтобы получить ссылку на ячейку LockFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислоккформат** <br/> |
   

