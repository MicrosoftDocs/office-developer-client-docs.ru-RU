---
title: Ячейка LockVtxEdit (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Блокирует грани фигуры, их нельзя изменить.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814170"
---
# <a name="lockvtxedit-cell-protection-section"></a>Ячейка LockVtxEdit (раздел Защита)

Блокирует грани фигуры, их нельзя изменить.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Невозможно изменить вершин.  <br/> |
|FALSE  <br/> |Можно изменять вершины.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LockVtxEdit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LockVtxEdit  <br/> |
   
Для получения ссылки на ячейки LockVtxEdit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLock** <br/> |
|Индекс ячейки:  <br/> |**visLockVtxEdit** <br/> |
   

