---
title: Alignment Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Задает выравнивание табуляции.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341540"
---
# <a name="alignment-cell-tabs-section"></a>Alignment Cell (Tabs Section)

Задает выравнивание табуляции.
  
|**Значение**|**Alignment**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Left  <br/> |**Вистабстоплефт** <br/> |
| 1,1  <br/> | Center  <br/> |**Вистабстопцентер** <br/> |
| 2  <br/> | Right  <br/> |**Вистабстопригхт** <br/> |
| 4  <br/> | Десятичное число  <br/> |**ВистабстопдеЦимал** <br/> |
| SP4  <br/> | Числ  <br/> |**Вистабстопкомма** <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку выравнивания по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Знаков.  *ИЖ* , где *i и j =* <1>, 2, 3  <br/> |
   
Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионтаб** <br/> |
| Индекс строки:  <br/> |**висровтаб +** ** где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j* * 3) **+ вистабалигн** <br/> |
   

