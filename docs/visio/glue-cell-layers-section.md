---
title: Glue Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Указывает, можно ли приклеить фигуры, принадлежащие к слою.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408518"
---
# <a name="glue-cell-layers-section"></a>Glue Cell (Layers Section)

Указывает, можно ли приклеить фигуры, принадлежащие к слою.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Клей включен.  <br/> |
|FALSE  <br/> |Клей отключен.  <br/> |
   
## <a name="remarks"></a>Примечания

Эта ячейка соответствует параметру **Glue** в диалоговом окне Layer  **Properties** (на вкладке **Главная,** в группе редактирования щелкните Слои **и** нажмите кнопку **Свойства слоя).** 
  
Чтобы получить ссылку на ячейку Клея по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Glue[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Клея по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visLayerGlue** <br/> |
   

