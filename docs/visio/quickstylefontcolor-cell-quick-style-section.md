---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Определяет цвет шрифта из быстрых стилей, которые текст фигуры наследует от активной темы, в виде integer от 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415028"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>QuickStyleFontColor Cell (Quick Style Section)

Определяет цвет шрифта из быстрых стилей, которые текст фигуры наследует от активной темы, в виде integer от 0-1. 
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |В тексте фигуры используется цвет темного шрифта.  <br/> |
|1  <br/> |В тексте фигуры используется цвет шрифта Light.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку QuickStyleFontColor** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | QuickStyleFontColor  <br/> |
   
Чтобы получить ссылку на **ячейку QuickStyleFontColor** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleFontColor** <br/> |
   

