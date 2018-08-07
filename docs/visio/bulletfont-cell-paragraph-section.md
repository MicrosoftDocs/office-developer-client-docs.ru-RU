---
title: Ячейка BulletFont (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Представляет номер шрифта, используемого для форматирования текста, когда указана строка пользовательского маркера и значение в ячейке маркера больше нуля.
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813327"
---
# <a name="bulletfont-cell-paragraph-section"></a>Ячейка BulletFont (раздел "Абзац")

Представляет номер шрифта, используемого для форматирования текста, когда указана строка пользовательского маркера и значение в ячейке маркера больше нуля. 
  
## <a name="remarks"></a>Замечания

Номера шрифтов зависят шрифты, установленные в системе. Если значение равно 0, а строка пользовательского маркера, шрифт, используемый совпадает с шрифт первого знака абзаца.
  
Чтобы получить ссылку на ячейку BulletFont по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.BulletFont [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки BulletFont по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visBulletFont** <br/> |
   

