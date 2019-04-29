---
title: Name Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Содержит имя рецензента документов.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417688"
---
# <a name="name-cell-reviewer-section"></a>Name Cell (Reviewer Section)

Содержит имя рецензента документов.
  
## <a name="remarks"></a>Примечания

 Это значение по умолчанию равно имени, указанному в поле **имя пользователя** на **вкладке Общие** диалогового **окна Параметры Visio** (перейдите на вкладку **файл** , щелкните **Параметры**, а затем выберите **Общие**). 
  
Чтобы получить ссылку на ячейку Name по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Reviewer.Name [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Name по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионревиевер** <br/> |
| Индекс строки:  <br/> |**висровревиевер** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висревиевернаме** <br/> |
   

