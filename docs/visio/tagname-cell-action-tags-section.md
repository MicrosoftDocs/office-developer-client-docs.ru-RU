---
title: Ячейка TagName (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Имя тега действия, который используется в качестве ключа для связывания тега действия с его действиями.
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814980"
---
# <a name="tagname-cell-action-tags-section"></a>Ячейка TagName (раздел "Теги действий")

Имя тега действия, который используется в качестве ключа для связывания тега действия с его действиями.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
## <a name="remarks"></a>Замечания

 Ячейка TagName в разделе Действие тегов работает вместе с TagName ячейки в разделе действия, чтобы связать тег действия с его действиями. Строки в разделе действия также TagName ячейки, и эти строки с тем же значением ячейки TagName как этой ячейке определения действий, выполняемых для этого тега действия. 
  
Чтобы получить ссылку на ячейку TagName по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . TagName где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки TagName по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagName** <br/> |
   

