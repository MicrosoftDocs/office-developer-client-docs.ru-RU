---
title: Ячейка LockReplace (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Указывает, является ли фигура может принимать участие в операции замены (в качестве целевого или фигуры замещения).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814138"
---
# <a name="lockreplace-cell-protection-section"></a>Ячейка LockReplace (раздел Защита)

Указывает, является ли фигура может принимать участие в операции замены (в качестве целевого или фигуры замещения). 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Фигура не может быть заменен или использовать в качестве замены фигуры.  <br/> Для фигуры на полотно кнопка **Изменить фигуру** отключена при выборе фигуры.  <br/> Фигуры в наборе элементов фигуры не отображается как фигуры замещения, при нажатии кнопки **Изменить фигуру** .  <br/> |
|FALSE  <br/> |Форму можно заменить или использовать в качестве замены фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LockReplace  <br/> |
   
Для получения ссылки на ячейки **LockReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockReplace** <br/> |
   
