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
description: Имя тега действия, который используется в качестве ключа для связываия тега действия с его действиями.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417912"
---
# <a name="tagname-cell-action-tags-section"></a>TagName Cell (Action Tags Section)

Имя тега действия, который используется в качестве ключа для связываия тега действия с его действиями.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

 Ячейка TagName в разделе "Теги действий" работает вместе с ячейкой TagName в разделе "Действия", чтобы связать тег действия с его действиями. Строки в разделе "Действия" также имеют ячейку TagName, а строки с тем же значением ячейки TagName, что и эта ячейка, определяют действия, которые необходимо принять для этого тега действия. 
  
Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *name*  . TagName, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку TagName по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagName** <br/> |
   

