---
title: Ячейка LockWidth (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Блокирует ширину фигуры таким образом, чтобы его ширина не изменяется при изменении размеров фигуры.
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814162"
---
# <a name="lockwidth-cell-protection-section"></a>Ячейка LockWidth (раздел "Защита")

Блокирует ширину фигуры таким образом, чтобы его ширина не изменяется при изменении размеров фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Ширина блокировки.  <br/> |
| FALSE  <br/> | Ширина не блокируется.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockWidth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockWidth  <br/> |
   
Для получения ссылки на ячейки LockWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockWidth** <br/> |
   

