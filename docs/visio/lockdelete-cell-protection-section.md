---
title: LockDelete Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Блокирует фигуру таким образом, чтобы ее нельзя было удалить.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423141"
---
# <a name="lockdelete-cell-protection-section"></a>LockDelete Cell (Protection Section)

Блокирует фигуру таким образом, чтобы ее нельзя было удалить.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Удаление фигуры невозможно  <br/> |
| FALSE  <br/> | Фигуру можно удалить.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockDelete по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockDelete  <br/> |
   
Чтобы получить ссылку на ячейку LockDelete по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлокк** <br/> |
| Индекс ячейки:  <br/> |**Вислоккделете** <br/> |
   

