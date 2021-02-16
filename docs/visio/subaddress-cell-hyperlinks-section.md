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
description: Указывает расположение в целевом документе, к который необходимо связать.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349324"
---
# <a name="subaddress-cell-hyperlinks-section"></a>SubAddress Cell (Hyperlinks Section)

Указывает расположение в целевом документе, к который необходимо связать.
  
## <a name="remarks"></a>Примечания

Например, если ячейка Address имеет имя Drawing1.vsdx, ячейка SubAddress может указать имя страницы, например "Page-3". Если ячейка Address является файлом Microsoft Excel "Samples.xlsx", значением этой ячейки может быть лист или диапазон в листе, например "Функции листа" или "Лист1! A1:D10". Если ячейка Address имеет значение ", значение этой ячейки может быть именоваемой привязкой в документе, например https://www.microsoft.com/office/ "solutions".
  
Вы также можете установить значение этой ячейки в диалоговом  окне  "Гиперссылки" (в группе "Ссылки" на вкладке "Вставка" щелкните **"Гиперссылка").** 
  
Чтобы получить ссылку на ячейку SubAddress по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылка.  *name*  . SubAddress where Hyperlink  *.name*  is the row name  <br/> |
   
Чтобы получить ссылку на ячейку **SubAddress** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkSubAddress** <br/> |
   

