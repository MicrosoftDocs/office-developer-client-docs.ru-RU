---
title: Ячейка IndRight (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Представляет расстояние, на котором все строки абзаца находятся от правого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ справа остается неизменным.
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813957"
---
# <a name="indright-cell-paragraph-section"></a>Ячейка IndRight (раздел "Абзац")

Представляет расстояние, на котором все строки абзаца находятся от правого поля блока текста. Это значение не зависит от масштаба документа. Если документа изменяется, отступ справа остается неизменным.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку IndRight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.IndRight [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки IndRight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentRight** <br/> |
   

