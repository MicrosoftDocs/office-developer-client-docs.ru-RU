---
title: EnableLineProps Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Определяет, включает ли стиль свойства строки.
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410002"
---
# <a name="enablelineprops-cell-style-properties-section"></a>EnableLineProps Cell (Style Properties Section)

Определяет, включает ли стиль свойства строки.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включай свойства строки.  <br/> |
|FALSE  <br/> |Исключить свойства строки.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку EnableLineProps по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EnableLineProps  <br/> |
   
Чтобы получить ссылку на ячейку EnableLineProps по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesLine** <br/> |
   

