---
title: Ячейка HAlign (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Определяет горизонтальное выравнивание текста в блоке текста фигуры.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813893"
---
# <a name="halign-cell-paragraph-section"></a>Ячейка HAlign (раздел "Абзац")

Определяет горизонтальное выравнивание текста в блоке текста фигуры.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Выравнивание по левому краю  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Center  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | По правому краю  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Выравнивание  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | Выровнять force  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Замечания

Выровнять интервала между слов в каждой строки, кроме последней строки абзаца для выравнивания как слева и справа от текста с помощью поля.
  
Выровнять force выравнивает каждой строки в абзаце, включая последний.
  
Чтобы получить ссылку на ячейку HAlign по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.HorzAlign [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки HAlign по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visHorzAlign** <br/> |
   

