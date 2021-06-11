---
title: SortKey Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Оценивает строку, которая влияет на порядок, в котором перечислены элементы в окне Shape Data.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417856"
---
# <a name="sortkey-cell-shape-data-section"></a>SortKey Cell (Shape Data Section)

Оценивает строку, которая влияет на порядок, в котором перечислены элементы в окне **Shape Data.** 
  
## <a name="remarks"></a>Примечания

Расчет, используемый для сравнения значений SortKey, является локальным и нечувствительным. Если значения SortKey равны, данные фигуры перечислены в порядке строки. Фигуры данных, не содержащих ключ сортировки, перечислены после данных фигуры, содержащих ключ сортировки.
  
Ниже приводится пример использования ключей сортировки для отображения данных фигуры в окне **Shape Data** в порядке: номер элемента, количество, цена. 
  
 *Строка, метка*  и  *SortKey*  относятся к ячейкам в строке данных фигуры. В этом случае строки данных фигуры были названы. 
  
|**Row**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Номер элемента  <br/> | 1  <br/> |
| Prop.Price  <br/> | ЦЕНА  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Количество  <br/> | 2  <br/> |
   
Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Prop.  *Имя*  . SortKey where Prop.  *Имя*  — это имя настраиваемой строки свойств  <br/> |
   
Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsSortKey** <br/> |
   

