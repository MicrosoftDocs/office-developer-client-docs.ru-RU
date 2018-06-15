---
title: Ячейка LockGroup (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Блокирует группу, его нельзя разгруппировать.
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814150"
---
# <a name="lockgroup-cell-protection-section"></a>Ячейка LockGroup (раздел Защита)

Блокирует группу, его нельзя разгруппировать.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Группа не может быть без группировки.  <br/> |
|FALSE  <br/> |Группа может быть без группировки.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение LockGroupCell значение TRUE, также будет отключено удаления любой фигуры, которые являются участниками группы.
  
Чтобы получить ссылку на ячейку LockGroup по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LockGroup  <br/> |
   
Для получения ссылки на ячейки LockGroup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLock** <br/> |
|Индекс ячейки:  <br/> |**visLockGroup** <br/> |
   

