---
title: SubAddress Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Указывает расположение в целевом документе, к которому необходимо перейти.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349324"
---
# <a name="subaddress-cell-hyperlinks-section"></a>SubAddress Cell (Hyperlinks Section)

Указывает расположение в целевом документе, к которому необходимо перейти.
  
## <a name="remarks"></a>Примечания

Например, если ячейка Address — "Drawing1. vsdx", в ячейке подадреса может быть указано имя страницы, например "Page-3". Если ячейка address — это файл Microsoft Excel "Samples. xlsx", то значение этой ячейки может быть листом или диапазоном на листе, например "функции листа" или "Лист1! A1: D10 ". Если ячейка Address — "https://www.microsoft.com/office/", значение этой ячейки может быть именованной точкой привязки в документе, например "Solutions".
  
Значение этой ячейки также можно задать в диалоговом окне **гиперссылки** (в группе **ссылки** на вкладке **Вставка** выберите **Гиперссылка**).
  
Чтобы получить ссылку на ячейку подадреса по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылки.  *Name (имя* ). Подадрес *, где имя ссылки является* именем строки  <br/> |
   
Чтобы получить ссылку на ячейку **Подадреса** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**виссектионхиперлинк** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**вишлинксубаддресс** <br/> |
   

