---
title: Ячейка IndLeft (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Представляет расстояние, на котором все строки абзаца находятся от левого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ слева остается неизменным.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813955"
---
# <a name="indleft-cell-paragraph-section"></a>Ячейка IndLeft (раздел "Абзац")

Представляет расстояние, на котором все строки абзаца находятся от левого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ слева остается неизменным.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку IndLeft по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.IndLeft [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки IndLeft по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentLeft** <br/> |
   

