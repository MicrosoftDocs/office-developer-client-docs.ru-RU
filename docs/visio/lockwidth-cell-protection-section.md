---
title: LockWidth Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Блокирует ширину фигуры так, чтобы ее ширина оставалась неизменной при размере фигуры.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439809"
---
# <a name="lockwidth-cell-protection-section"></a>LockWidth Cell (Protection Section)

Блокирует ширину фигуры так, чтобы ее ширина оставалась неизменной при размере фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Ширина заблокирована.  <br/> |
| FALSE  <br/> | Ширина не заблокирована.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockWidth по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockWidth  <br/> |
   
Чтобы получить ссылку на ячейку LockWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockWidth** <br/> |
   

