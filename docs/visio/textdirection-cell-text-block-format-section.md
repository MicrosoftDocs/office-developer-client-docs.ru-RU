---
title: Ячейка TextDirection (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Определяет направление символов в блоке текста.
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815021"
---
# <a name="textdirection-cell-text-block-format-section"></a>Ячейка TextDirection (раздел "Формат текстового блока")

Определяет направление символов в блоке текста.
  
|**Значение**|**Direction**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Горизонтальная  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | По вертикали  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Замечания

В продуктах японского языка версии 5.0 Visio значение ячейки была сохранена в ячейке VerticalText в разделе Разное.
  
Чтобы получить ссылку на ячейку TextDirection по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | TextDirection  <br/> |
   
Для получения ссылки на ячейки TextDirection по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkDirection** <br/> |
   

