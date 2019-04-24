---
title: TagName Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Имя тега действия, используемого в качестве ключа для сопоставления тега действия с его действиями.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332398"
---
# <a name="tagname-cell-action-tags-section"></a>TagName Cell (Action Tags Section)

Имя тега действия, используемого в качестве ключа для сопоставления тега действия с его действиями.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

 Ячейка TagName в разделе "теги действий" работает вместе с ячейкой TagName в разделе "действия", чтобы связать тег действия с его действиями. В строках раздела Actions также есть ячейка TagName, и эти строки с одинаковым значением ячейки TagName в этой ячейке определяют действия, выполняемые для этого тега действия. 
  
Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *Name (имя* ). TagName, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**Виссмарттагнаме** <br/> |
   

