---
title: Ячейка SpAfter (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Определяет дискового пространства вставленный после каждого абзаца в блоке текста фигуры пробелов из ячейки сплайн и, если он установлен в последний абзац текстового заблокировать, BottomMargin ячейки.
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814950"
---
# <a name="spafter-cell-paragraph-section"></a>Ячейка SpAfter (раздел "Абзац")

Определяет дискового пространства вставленный после каждого абзаца в блоке текста фигуры пробелов из ячейки сплайн и, если он установлен в последний абзац текстового заблокировать, BottomMargin ячейки.
  
## <a name="remarks"></a>Замечания

Это значение не зависит от масштаба документа. Если документа изменяется, пространство после параметр остается неизменным.
  
Чтобы получить ссылку на ячейку SpAfter по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.SpAfter [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки SpAfter по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSpaceAfter** <br/> |
   

