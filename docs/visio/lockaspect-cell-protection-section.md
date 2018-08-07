---
title: Ячейка LockAspect (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Блокирует пропорции фигуры, форму можно изменять только пропорционально. не может иметь размер одного измерения.
ms.openlocfilehash: fb5736add65f548f06697077bc539ec7fac5feb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814124"
---
# <a name="lockaspect-cell-protection-section"></a>Ячейка LockAspect (раздел "Защита")

Блокирует пропорции фигуры, форму можно изменять только пропорционально. не может иметь размер одного измерения.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Заблокированный пропорции.  <br/> |
| FALSE  <br/> | Отношение сторон не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockAspect по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockAspect  <br/> |
   
Для получения ссылки на ячейки LockAspect по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockAspect** <br/> |
   

