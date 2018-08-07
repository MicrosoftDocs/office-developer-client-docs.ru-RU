---
title: Ячейка DocLockDuplicatePage (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Определяет ли страниц в документе может быть реализовано, типа Boolean.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813624"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Ячейка DocLockDuplicatePage (раздел "Свойства документа")

Определяет ли страниц в документе может быть реализовано, типа Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Дублируется** в контекстное меню страницы и метод автоматизации **Page.Duplicate** оба отключены.  <br/> |
|FALSE  <br/> |Страница может быть реализовано.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **DocLockDuplicatePage** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DocLockDuplicatePage  <br/> |
   
Для получения ссылки на ячейки **DocLockDuplicatePage** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocLockDuplicatePage** <br/> |
   

