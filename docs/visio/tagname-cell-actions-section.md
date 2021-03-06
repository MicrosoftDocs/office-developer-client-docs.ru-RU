---
title: TagName Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Содержит имя тега действия, с которого связано это действие.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412718"
---
# <a name="tagname-cell-actions-section"></a>TagName Cell (Actions Section)

Содержит имя тега действия, с которого связано это действие.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Ячейка TagName в разделе Действия работает вместе с ячейкой TagName в разделе Теги действий, чтобы связать тег действий с его действиями. 
  
- Если ячейка TagName в строке Действия пуста, действие отображается в меню ярлыка, а не в меню тегов действий.
    
- Если значение ячейки TagName в строке Действия совпадает со значением ячейки TagName в строке Smart Tags, действие отображается в меню тегов действий.
    
- Если ячейка TagName действия имеет значение, но не соответствует значению TagName в строке тегов фигуры, это действие не появляется в меню тегов действий или меню ярлыка.
    
- Если несколько смарт-строк тегов имеют одинаковое значение TagName, все они будут показывать одинаковые действия.
    
Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *имя*  . Действия TagNamewhere.  *имя*  — это имя строки Действия  <br/> |
   
Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visActionTagName** <br/> |
   

