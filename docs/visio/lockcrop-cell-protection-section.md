---
title: Ячейка LockCrop (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Блокирует объект из другой программы от обрезки с помощью Обрезка.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814125"
---
# <a name="lockcrop-cell-protection-section"></a>Ячейка LockCrop (раздел "Защита")

Блокирует объект из другой программы от обрезки с помощью **Обрезка** . 
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не удается обрезки фигуры  <br/> |
| FALSE  <br/> | Фигура может быть обрезки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockCrop по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockCrop  <br/> |
   
Для получения ссылки на ячейки LockCrop по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockCrop** <br/> |
   

