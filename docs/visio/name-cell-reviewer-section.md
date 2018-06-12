---
title: Имя ячейки (редактор раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Содержит имя рецензент документа.
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814294"
---
# <a name="name-cell-reviewer-section"></a>Имя ячейки (редактор раздел)

Содержит имя рецензент документа.
  
## <a name="remarks"></a>Замечания

 Значение по умолчанию на имя в поле **имя пользователя** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , нажмите кнопку **Параметры**и выберите пункт **Общие**). 
  
Чтобы получить ссылку на имя ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Reviewer.Name [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Чтобы получить ссылку на имя ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionReviewer** <br/> |
| Индекс строки:  <br/> |**visRowReviewer** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visReviewerName** <br/> |
   

