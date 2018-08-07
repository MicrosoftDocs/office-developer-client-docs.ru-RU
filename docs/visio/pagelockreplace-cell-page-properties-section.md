---
title: Ячейка PageLockReplace (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Указывает, будет ли кнопку Заменить фигуру запрещено на этой странице.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814341"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Ячейка PageLockReplace (раздел "Свойства страницы")

Указывает, будет ли кнопку **Заменить фигуру** запрещено на этой странице. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Кнопка **Изменить фигуру** недоступна при активной на этой странице.  <br/> |
|FALSE  <br/> |Кнопка **Изменить фигуру** по на этой странице не отключен. Кнопки по-прежнему могут быть недоступны if: **DocLockReplace** на **DocumentSheet** задано значение **TRUE**; Ячейка **LockReplace** для выбранной фигуры присвоено **значение TRUE**.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **PageLockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageLockReplace  <br/> |
   
Для получения ссылки на ячейки **PageLockReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageLockReplace** <br/> |
   

