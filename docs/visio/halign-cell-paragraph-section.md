---
title: HAlign Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Определяет горизонтальное выравнивание текста в текстовом блоке фигуры.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414741"
---
# <a name="halign-cell-paragraph-section"></a>HAlign Cell (Paragraph Section)

Определяет горизонтальное выравнивание текста в текстовом блоке фигуры.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Выравнивание по левую  <br/> |**visHorzLeft** <br/> |
| 1   <br/> | Center  <br/> |**visHorzCenter** <br/> |
| 2   <br/> | Выравнивание по правому направлению  <br/> |**visHorzRight** <br/> |
| 3   <br/> | Justify  <br/> |**visHorzJustify** <br/> |
| 4   <br/> | Принудительное обоснование  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Примечания

Justify добавляет пробел между словами в каждой строке, кроме последней строки абзаца, чтобы выровнять левую и правую части текста с полями.
  
Принудительное обоснование обустроит каждую строку абзаца, включая последнюю.
  
Чтобы получить ссылку на ячейку HAlign по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.HorzAlign[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку HAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHorzAlign** <br/> |
   

