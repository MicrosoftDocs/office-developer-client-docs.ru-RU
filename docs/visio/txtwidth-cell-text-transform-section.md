---
title: Ячейка ШиринаТекста (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Определяет ширину блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815100"
---
# <a name="txtwidth-cell-text-transform-section"></a>Ячейка ШиринаТекста (раздел Преобразование текст)

Определяет ширину блока текста. Формула по умолчанию имеет вид:
  
= Ширина \* 1
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ШиринаТекста по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ШиринаТекста  <br/> |
   
Для получения ссылки на ячейки ШиринаТекста по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormWidth** <br/> |
   

