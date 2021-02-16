---
title: Initials Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Содержит инициалы рецензента документов.
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411507"
---
# <a name="initials-cell-reviewer-section"></a>Initials Cell (Reviewer Section)

Содержит инициалы рецензента документов.
  
## <a name="remarks"></a>Примечания

Это значение по умолчанию является  инициалами  в поле "Инициалы" на  вкладке "Общие" в диалоговом окне "Параметры **Visio"** (щелкните вкладку "Файл", выберите "Параметры" и выберите **"Общие").** 
  
Чтобы получить ссылку на ячейку Initials по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Reviewer.Initials [  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Initials по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionReviewer** <br/> |
| Индекс строки:  <br/> |**visRowReviewer**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visReviewerInitials** <br/> |
   

