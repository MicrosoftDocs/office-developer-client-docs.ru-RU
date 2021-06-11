---
title: Print Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Указывает, можно ли печатать фигуры, принадлежащие к слою.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435217"
---
# <a name="print-cell-layers-section"></a>Print Cell (Layers Section)

Указывает, можно ли печатать фигуры, принадлежащие к слою.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Фигуры можно распечатать.  <br/> |
|FALSE  <br/> |Фигуры не могут быть напечатаны.  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение можно также установить с помощью параметра **Печать** в диалоговом окне **Свойства** слоя (на вкладке Home, в группе редактирования щелкните Слои и нажмите кнопку **Свойства слоя).**   
  
Чтобы получить ссылку на ячейку Print по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Print[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Print по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visDocPreviewScope** <br/> |
   

