---
title: Ячейка LockFromGroupFormat (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814145"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Ячейка LockFromGroupFormat (раздел Защита)

Блоки изменений формата групповой фигуры распространения на вложенные фигуры, при этом позволяя пользователям напрямую форматирование указанных вложенных фигур. 
  
Значение ячейки LockFromGroupFormat соответствует параметру **из группы форматирования** флажок в диалоговом окне " **Защита** ". 
  
Для ссылки на ячейки LockFromGroupFormat по имени из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LockFromGroupFormat  <br/> |
   
Для ссылки на ячейки LockFromGroupFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLock** <br/> |
|Индекс ячейки:  <br/> |**visLockFromGroupFormat** <br/> |
   
Значение по умолчанию для ячейки равно 0 (False).
  

