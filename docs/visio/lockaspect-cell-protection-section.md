---
title: LockAspect Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Блокирует пропорции фигуры, чтобы ее размер был пропорционально; его размер не может быть замеизирован в одном измерении.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411584"
---
# <a name="lockaspect-cell-protection-section"></a>LockAspect Cell (Protection Section)

Блокирует пропорции фигуры, чтобы ее размер был пропорционально; Его нельзя масштабовать в одном измерении.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Пропорции заблокированы.  <br/> |
| FALSE  <br/> | Пропорции не заблокированы.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockAspect по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockAspect  <br/> |
   
Чтобы получить ссылку на ячейку LockAspect по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockAspect** <br/> |
   

