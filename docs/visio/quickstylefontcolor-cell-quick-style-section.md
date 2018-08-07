---
title: Ячейка QuickStyleFontColor (раздел "Экспресс-стиль")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Определяет цвет шрифта из экспресс-стилей, который текстом фигуры наследует от активной темы, как целое число от 0-1.
ms.openlocfilehash: 8f2d77508dccffccf472f8ab80517e840f860541
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814509"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>Ячейка QuickStyleFontColor (раздел "Экспресс-стиль")

Определяет цвет шрифта из экспресс-стилей, который текстом фигуры наследует от активной темы, как целое число от 0-1. 
  
|||
|:-----|:-----|
|Значение  <br/> |Описание  <br/> |
|0  <br/> |В тексте фигуры используется темный цвет.  <br/> |
|1  <br/> |В тексте фигуры используется светлый цвет.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **QuickStyleFontColor** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | QuickStyleFontColor  <br/> |
   
Для получения ссылки на ячейки **QuickStyleFontColor** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleFontColor** <br/> |
   

