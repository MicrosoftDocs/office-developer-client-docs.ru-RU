---
title: Strikethru Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Определяет, отформатирован ли текст с зачеркиванием.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349338"
---
# <a name="strikethru-cell-character-section"></a>Strikethru Cell (Character Section)

Определяет, отформатирован ли текст с зачеркиванием.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Текст форматируется с зачеркиванием.  <br/> |
|FALSE  <br/> |Текст не отформатирован с зачеркиванием.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этой ячейки также можно задать с помощью диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ). 
  
Чтобы получить ссылку на ячейку Strikethru по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Char. Strikethru [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Strikethru по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**Виссектиончарактер** <br/> |
|Индекс строки:  <br/> |**висровчарактер** +  *i* , где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**Висчарактерстрикесру** <br/> |
   

