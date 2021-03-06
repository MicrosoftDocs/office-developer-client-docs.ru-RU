---
title: TextDirection Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Определяет направление символов в текстовом блоке.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406229"
---
# <a name="textdirection-cell-text-block-format-section"></a>TextDirection Cell (Text Block Format Section)

Определяет направление символов в текстовом блоке.
  
|**Значение**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Горизонтальный  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Вертикальный  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Примечания

В Visio версии 5.0 японской продукции значение этой ячейки хранилось в ячейке VerticalText в разделе Разное.
  
Чтобы получить ссылку на ячейку TextDirection по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | TextDirection  <br/> |
   
Чтобы получить ссылку на ячейку TextDirection по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkDirection** <br/> |
   

