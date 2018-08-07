---
title: Ячейка Initials (раздел "Рецензент")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Содержит инициалы рецензент документа.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813973"
---
# <a name="initials-cell-reviewer-section"></a>Ячейка Initials (раздел "Рецензент")

Содержит инициалы рецензент документа.
  
## <a name="remarks"></a>Замечания

Значением по умолчанию инициалы в поле **Инициалы** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , нажмите кнопку **Параметры**и выберите пункт **Общие** ). 
  
Для получения ссылки на ячейки инициалы по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Reviewer.Initials [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки инициалы по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionReviewer** <br/> |
| Индекс строки:  <br/> |**visRowReviewer** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visReviewerInitials** <br/> |
   

