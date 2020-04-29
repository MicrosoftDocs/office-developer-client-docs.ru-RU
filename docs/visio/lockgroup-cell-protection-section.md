---
title: LockGroup Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Блокирует группу, чтобы ее нельзя было разгруппировать.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404311"
---
# <a name="lockgroup-cell-protection-section"></a>LockGroup Cell (Protection Section)

Блокирует группу, чтобы ее нельзя было разгруппировать.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Группа не может быть разгруппирована.  <br/> |
|FALSE  <br/> |Группу можно разгруппировать.  <br/> |
   
## <a name="remarks"></a>Примечания

При установке значения TRUE для Локкграупцелл также запрещается удаление всех фигур, которые являются членами группы.
  
Чтобы получить ссылку на ячейку LockGroup по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LockGroup  <br/> |
   
Чтобы получить ссылку на ячейку LockGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровлокк** <br/> |
|Индекс ячейки:  <br/> |**вислоккграуп** <br/> |
   

