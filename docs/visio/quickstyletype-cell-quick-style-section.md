---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Определяет тип экспресс-стиля (2-мерный, 1-мерный или соединитель), наследуемого формой.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410506"
---
# <a name="quickstyletype-cell-quick-style-section"></a>QuickStyleType Cell (Quick Style Section)

Определяет тип экспресс-стиля (2-мерный, 1-мерный или соединитель), наследуемого формой. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Visio выбирает автоматически  <br/> |
|1,1  <br/> |1 измерение  <br/> |
|2  <br/> |2 измерения  <br/> |
|4  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **QuickStyleType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | QuickStyleType  <br/> |
   
Чтобы получить ссылку на ячейку **QuickStyleType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровкуиккстилепропертиес** <br/> |
| Индекс ячейки:  <br/> |**Вискуиккстилетипе** <br/> |
   

