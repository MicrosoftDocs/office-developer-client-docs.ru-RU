---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Определяет, можно ли дублировать страницы в документе в качестве boolean.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439662"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage Cell (Document Properties Section)

Определяет, можно ли дублировать страницы в документе в качестве boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Дубликаты** в меню ярлыка страницы и метод **автоматизации Page.Duplicate** отключены.  <br/> |
|FALSE  <br/> |Страницу можно дублировать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **DocLockDuplicatePage** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DocLockDuplicatePage  <br/> |
   
Чтобы получить ссылку на ячейку **DocLockDuplicatePage** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocLockDuplicatePage** <br/> |
   

