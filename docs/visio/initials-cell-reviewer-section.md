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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335296"
---
# <a name="initials-cell-reviewer-section"></a>Initials Cell (Reviewer Section)

Содержит инициалы рецензента документов.
  
## <a name="remarks"></a>Комментарии

Это значение по умолчанию задается в поле **инициалы** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , щелкните **Параметры**, а затем выберите **Общие** ). 
  
Чтобы получить ссылку на ячейку инициалов по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Review. инициалы [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку инициалов по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионревиевер** <br/> |
| Индекс строки:  <br/> |**висровревиевер** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висревиеверинитиалс** <br/> |
   

