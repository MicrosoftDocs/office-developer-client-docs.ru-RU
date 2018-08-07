---
title: Ячейка QuickStyleType (раздел "Экспресс-стиль")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Определяет тип экспресс-стилей (2 измерения, 1 измерения или соединитель), который наследует фигуры.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814514"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Ячейка QuickStyleType (раздел "Экспресс-стиль")

Определяет тип экспресс-стилей (2 измерения, 1 измерения или соединитель), который наследует фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Автоматически выбирает Visio  <br/> |
|1  <br/> |измерения 1  <br/> |
|2  <br/> |2 измерения  <br/> |
|3  <br/> |Соединитель  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **QuickStyleType** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | QuickStyleType  <br/> |
   
Для получения ссылки на ячейки **QuickStyleType** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowQuickStyleProperties** <br/> |
| Индекс ячейки:  <br/> |**visQuickStyleType** <br/> |
   

