---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Указывает, следует ли отключить кнопку Replace Shape для этой страницы.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433103"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace Cell (Page Properties Section)

Указывает, следует ли отключить кнопку **Replace Shape** для этой страницы. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Кнопка **Изменение формы** от серый, когда эта страница активна.  <br/> |
|FALSE  <br/> |Кнопка **Изменение формы** не отключена этой страницей. Кнопка по-прежнему может быть посеяна, если: **docLockReplace** на **таблице DocumentSheet** за установлено **true;** Ячейка **LockReplace** для выбранной фигуры установлена в **TRUE**.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на **ячейку PageLockReplace** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLockReplace  <br/> |
   
Чтобы получить ссылку на **ячейку PageLockReplace** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageLockReplace** <br/> |
   

