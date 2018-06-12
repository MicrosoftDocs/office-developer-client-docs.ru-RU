---
title: Ячейка TxtLocPinX (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Определяет значение x-координаты центра блок текста из ротации относительно начала блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815067"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Ячейка TxtLocPinX (раздел Преобразование текст)

Определяет значение *x* -координаты центра блок текста из ротации относительно начала блока текста. Формула по умолчанию имеет вид: 
  
= ШиринаТекста \* 0,5
  
Эту формулу вычисляется по горизонтали по центру блока текста.
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку TxtLocPinX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TxtLocPinX  <br/> |
   
Для получения ссылки на ячейки TxtLocPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowTextXForm** <br/> |
| Индекс ячейки:  <br/> |**visXFormLocPinX** <br/> |
   

