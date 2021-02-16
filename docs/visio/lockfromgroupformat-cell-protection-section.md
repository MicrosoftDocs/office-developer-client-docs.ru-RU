---
title: LockFromGroupFormat Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426060"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>LockFromGroupFormat Cell (Protection Section)

Блокирует распространение изменений формата в фигуры группы на подформы, при этом позволяя пользователям форматировать выбранные под фигуры напрямую. 
  
Значение ячейки LockFromGroupFormat соответствует параметру "От" в диалоговом окне "Защита".   
  
Чтобы сослаться на ячейку LockFromGroupFormat по имени из другой формулы или из программы, используя свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LockFromGroupFormat  <br/> |
   
Чтобы сослаться на ячейку LockFromGroupFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowLock** <br/> |
|Индекс ячейки:  <br/> |**visLockFromGroupFormat** <br/> |
   
Значение по умолчанию для ячейки — 0 (False).
  

