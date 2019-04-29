---
title: VerticalAlign Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Определяет вертикальное выравнивание текста в блоке текста.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425794"
---
# <a name="verticalalign-cell-text-block-format-section"></a>VerticalAlign Cell (Text Block Format Section)

Определяет вертикальное выравнивание текста в блоке текста.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Top  <br/> |**Висверттоп** <br/> |
| 1,1  <br/> | Назван  <br/> |**Висвертмиддле** <br/> |
| 2  <br/> | Конец  <br/> |**Висвертботтом** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку VerticalAlign по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | VerticalAlign  <br/> |
   
Чтобы получить ссылку на ячейку VerticalAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровтекст** <br/> |
| Индекс ячейки:  <br/> |**Висткстблквертикалалигн** <br/> |
   

