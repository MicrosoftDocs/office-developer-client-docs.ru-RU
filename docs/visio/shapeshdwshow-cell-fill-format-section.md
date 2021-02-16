---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, отображает ли фигура тень в виде integer от 0 до 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422119"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format Section)

Определяет, отображает ли фигура тень в виде integer от 0 до 2.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Всегда отображает тень, если она указана. Тени для под фигур не отображаются.  <br/> |
|1   <br/> |Не отрисовый тени, если у фигуры нет родительского. Используйте тени под фигур, если их сгруппировали.  <br/> |
|2   <br/> |Всегда отображать тень, если она указана. Отображаются тени для под фигур.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ShapeShdwShow** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShapeShdwShow  <br/> |
   
Чтобы получить ссылку на ячейку **ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowFill** <br/> |
| Индекс ячейки:  <br/> |**visFillShdwShow** <br/> |
   

