---
title: LockBegin Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Блокирует точку начала (BeginX, BeginY) формы 1-D в определенное расположение.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407762"
---
# <a name="lockbegin-cell-protection-section"></a>LockBegin Cell (Protection Section)

Блокирует точку начала (BeginX, BeginY) формы 1-D в определенное расположение.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Точка начала заблокирована.  <br/> |
| FALSE  <br/> | Начало не заблокировано.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockBegin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockBegin  <br/> |
   
Чтобы получить ссылку на ячейку LockBegin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockBegin** <br/> |
   

