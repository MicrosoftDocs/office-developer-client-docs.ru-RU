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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425542"
---
# <a name="alignment-cell-tabs-section"></a>Alignment Cell (Tabs Section)

Задает выравнивание табуляции.
  
|**Значение**|**Alignment**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Left  <br/> |**вистабстоплефт** <br/> |
| 1,1  <br/> | Center  <br/> |**вистабстопцентер** <br/> |
| 2  <br/> | Right  <br/> |**вистабстопригхт** <br/> |
| 4  <br/> | Десятичное число  <br/> |**вистабстопдеЦимал** <br/> |
| 4   <br/> | Числ  <br/> |**вистабстопкомма** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку выравнивания по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Знаков.  *ИЖ* , где *i и j =* <1>, 2, 3  <br/> |
   
Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**виссектионтаб** <br/> |
| Индекс строки:  <br/> |**висровтаб +** *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> | (*j* * 3) **+ вистабалигн** <br/> |
   

