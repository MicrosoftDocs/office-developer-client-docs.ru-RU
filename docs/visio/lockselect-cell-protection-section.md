---
title: LockSelect Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Предотвращает выбор фигуры.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409757"
---
# <a name="lockselect-cell-protection-section"></a>LockSelect Cell (Protection Section)

Предотвращает выбор фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Форма не может быть выбрана.  <br/> |
| FALSE  <br/> | Фигура может быть выбрана.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы LockSelect вступил в силу, в диалоговом окне Protect **Document** необходимо выбрать поле **"Формы".** 
  
Чтобы получить ссылку на ячейку LockSelect по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockSelect  <br/> |
   
Чтобы получить ссылку на ячейку LockSelect по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockSelect** <br/> |
   

