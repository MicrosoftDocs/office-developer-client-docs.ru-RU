---
title: Menu Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Определяет имя элемента меню, которое отображается в ярлыке или меню тегов действий для фигуры или страницы.
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436330"
---
# <a name="menu-cell-actions-section"></a>Menu Cell (Actions Section)

Определяет имя элемента меню, которое отображается в ярлыке или меню тегов действий для фигуры или страницы. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Чтобы вставить в меню над этим элементом элемент сепаратор, используйте ячейку BeginGroup. Чтобы отобразить команду в нижней части меню, применив к имени символ процента (%).
  
Чтобы получить ссылку на ячейку Menu по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *name*  . Действия в меню.  *имя*  — это имя строки "Действия".  <br/> |
   
Чтобы получить ссылку на ячейку Меню по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i* где i = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visActionMenu** <br/> |
   

