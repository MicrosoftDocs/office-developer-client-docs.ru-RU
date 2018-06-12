---
title: Ячейка ВысотаТекста (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Определяет высоту блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815080"
---
# <a name="txtheight-cell-text-transform-section"></a>Ячейка ВысотаТекста (раздел Преобразование текст)

Определяет высоту блока текста. Формула по умолчанию имеет вид:
  
= Высота \* 1
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ВысотаТекста по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ВысотаТекста  <br/> |
   
Для получения ссылки на ячейки ВысотаТекста по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormHeight** <br/> |
   

