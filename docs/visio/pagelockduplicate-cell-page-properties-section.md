---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Определяет, можно ли дублировать страницу в качестве логического значения.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283666"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties Section)

Определяет, можно ли дублировать страницу в качестве логического значения.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Дублировать** в контекстном меню страницы и на **странице.** для этой страницы оба метода автоматизации для дубликатов отключены.  <br/> |
|FALSE  <br/> |Страница может дублироваться.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку **PageLockDuplicate** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLockDuplicate  <br/> |
   
Чтобы получить ссылку на ячейку **PageLockDuplicate** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпаже** <br/> |
| Индекс ячейки:  <br/> |**Виспажелоккдупликате** <br/> |
   

