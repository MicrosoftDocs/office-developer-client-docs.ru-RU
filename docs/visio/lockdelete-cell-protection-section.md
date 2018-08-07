---
title: Ячейка LockDelete (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Блокирует фигуру таким образом, чтобы он не может быть удален.
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814128"
---
# <a name="lockdelete-cell-protection-section"></a>Ячейка LockDelete (раздел "Защита")

Блокирует фигуру таким образом, чтобы он не может быть удален.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура не может быть удалена  <br/> |
| FALSE  <br/> | Фигура может быть удалена.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockDelete по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockDelete  <br/> |
   
Для получения ссылки на ячейки LockDelete по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockDelete** <br/> |
   

