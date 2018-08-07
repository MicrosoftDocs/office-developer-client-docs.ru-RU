---
title: Ячейка PageLockDuplicate (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Определяет, будет ли страница может быть реализовано, как логическое значение.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814335"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Ячейка PageLockDuplicate (раздел "Свойства страницы")

Определяет, будет ли страница может быть реализовано, как логическое значение.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Дублируется** в контекстное меню страницы и метод автоматизации **Page.Duplicate** оба отключены для страницы.  <br/> |
|FALSE  <br/> |Страница может быть реализовано.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **PageLockDuplicate** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageLockDuplicate  <br/> |
   
Для получения ссылки на ячейки **PageLockDuplicate** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageLockDuplicate** <br/> |
   

