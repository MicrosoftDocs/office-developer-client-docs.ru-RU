---
title: Ячейка IndFirst (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Представляет расстояние от левого отступа для абзаца с отступом первой строки каждого абзаца в блоке текста фигуры. Это значение не зависит от масштаба документа. Если документа изменяется, отступ первой строки остается неизменным.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813946"
---
# <a name="indfirst-cell-paragraph-section"></a>Ячейка IndFirst (раздел "Абзац")

Представляет расстояние от левого отступа для абзаца с отступом первой строки каждого абзаца в блоке текста фигуры. Это значение не зависит от масштаба документа. Если документа изменяется, отступ первой строки остается неизменным.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку IndFirst по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.IndFirst [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки IndFirst по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentFirst** <br/> |
   

