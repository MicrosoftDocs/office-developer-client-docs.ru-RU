---
title: Ячейка EnableTextProps (раздел "Свойства стиля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Определяет, включены ли в стиль свойства текста.
ms.openlocfilehash: a51f83624192615e84292129d4788ae1e2779c6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813683"
---
# <a name="enabletextprops-cell-style-properties-section"></a>Ячейка EnableTextProps (раздел "Свойства стиля")

Определяет, включены ли в стиль свойства текста.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включайте свойства текста.  <br/> |
|FALSE  <br/> |Исключение свойства текста.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку EnableTextProps по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |EnableTextProps  <br/> |
   
Для получения ссылки на ячейки EnableTextProps по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesText** <br/> |
   

