---
title: Ячейка Action (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Содержит формулу для выполнения, если пользователь выбирает команду меню тега ярлык или действие.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813127"
---
# <a name="action-cell-actions-section"></a>Ячейка Action (раздел "Действия")

Содержит формулу для выполнения, если пользователь выбирает команду меню тега ярлык или действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
## <a name="remarks"></a>Замечания

В действие ячейки вычисляется только в том случае, когда происходит действие, не при вводе формулы.
  
Для получения ссылки на ячейки действие по имени из другой формулы или из файла с помощью свойства **CellsU** использования: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Действия.  *имя* . Действие которых действия. *имя* — это имя строки действий  <br/> |
   
Для получения ссылки на ячейки thethe действие по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAction** <br/> |
| Индекс строки:  <br/> |**visRowAction** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visActionAction** <br/> |
   

