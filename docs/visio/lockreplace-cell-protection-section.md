---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Указывает, может ли фигура участвовать в операции замены (в качестве цели или формы замены).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404143"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection Section)

Указывает, может ли фигура участвовать в операции замены (в качестве цели или формы замены). 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Фигура не может быть заменена или использоваться в качестве замены.  <br/> Для фигуры на холсте кнопка **Изменить форму** отключена при выборе фигуры.  <br/> Для фигуры на трафарете фигура не появляется в качестве формы замены при нажатии кнопки **Изменить** форму.  <br/> |
|FALSE  <br/> |Фигуру можно заменить или использовать в качестве замены.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **LockReplace** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockReplace  <br/> |
   
Чтобы получить ссылку на ячейку **LockReplace** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockReplace** <br/> |
   

