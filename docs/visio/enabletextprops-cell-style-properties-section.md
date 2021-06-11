---
title: EnableTextProps Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Определяет, включает ли стиль текстовые свойства.
ms.openlocfilehash: 3f1d87316955b4e6e40cea16634cff7645a720fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419263"
---
# <a name="enabletextprops-cell-style-properties-section"></a>EnableTextProps Cell (Style Properties Section)

Определяет, включает ли стиль текстовые свойства.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включаем свойства текста.  <br/> |
|FALSE  <br/> |Исключить свойства текста.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку EnableTextProps по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EnableTextProps  <br/> |
   
Чтобы получить ссылку на ячейку EnableTextProps по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesText** <br/> |
   

