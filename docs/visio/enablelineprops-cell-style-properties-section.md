---
title: Ячейка EnableLineProps (раздел "Свойства стиля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Определяет, включены ли в стиль свойства линии.
ms.openlocfilehash: 0e1eb67528b3e87bcfff5281dd1e0b2db3a0a4d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813681"
---
# <a name="enablelineprops-cell-style-properties-section"></a>Ячейка EnableLineProps (раздел "Свойства стиля")

Определяет, включены ли в стиль свойства линии.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включайте свойства строки.  <br/> |
|FALSE  <br/> |Исключение свойства строки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку EnableLineProps по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |EnableLineProps  <br/> |
   
Для получения ссылки на ячейки EnableLineProps по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesLine** <br/> |
   

