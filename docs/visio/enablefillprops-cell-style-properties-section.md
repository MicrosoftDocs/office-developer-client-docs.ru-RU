---
title: EnableFillProps Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Определяет, включает ли стиль свойства заливки.
ms.openlocfilehash: 55191cb28d5777f7fb65a3a1e4be890e6dda4e8b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406012"
---
# <a name="enablefillprops-cell-style-properties-section"></a>EnableFillProps Cell (Style Properties Section)

Определяет, включает ли стиль свойства заливки.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включите свойства заливки.  <br/> |
|FALSE  <br/> |Исключить свойства заливки.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку EnableFillProps по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |EnableFillProps  <br/> |
   
Чтобы получить ссылку на ячейку EnableFillProps по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesFill** <br/> |
   

