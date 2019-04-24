---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, отображается ли в фигуре тень как целое число от 0 до 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349149"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format Section)

Определяет, отображается ли в фигуре тень как целое число от 0 до 2.
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Всегда отображать тень, если указана теневая копия. Тени для дочерних фигур не отображаются.  <br/> |
|1,1  <br/> |Не выводите тень, если у фигуры нет родительского объекта. Используйте тени вложенных фигур, если они сгруппированы вместе.  <br/> |
|2  <br/> |Всегда отображать тень, если указана тень. Отображаются тени для дочерних фигур.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ShapeShdwShow** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShapeShdwShow  <br/> |
   
Чтобы получить ссылку на ячейку **ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровфилл** <br/> |
| Индекс ячейки:  <br/> |**Висфиллшдвшов** <br/> |
   

