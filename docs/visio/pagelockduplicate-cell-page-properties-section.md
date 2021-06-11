---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Определяет, можно ли продублировать страницу в качестве boolean.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425983"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties Section)

Определяет, можно ли продублировать страницу в качестве boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Дубликат** в меню ярлыка страницы и метод автоматизации **Page.Duplicate** отключены для страницы.  <br/> |
|FALSE  <br/> |Страницу можно дублировать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку PageLockDuplicate** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLockDuplicate  <br/> |
   
Чтобы получить ссылку на **ячейку PageLockDuplicate** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageLockDuplicate** <br/> |
   

