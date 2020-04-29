---
title: ScaleY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Указывает процентное отношение увеличения страницы документа на странице принтера.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406992"
---
# <a name="scaley-cell-print-properties-section"></a>ScaleY Cell (Print Properties Section)

Указывает процентное отношение увеличения страницы документа на странице принтера.
  
## <a name="remarks"></a>Примечания

Это значение используется только в том случае, если ячейка onpage имеет значение FALSE. Ячейки ScaleX и Scale всегда имеют одинаковое значение, которое соответствует значению, указанному в параметре **изменить** на вкладке **Настройка печати** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **настройки страницы** ). 
  
Чтобы получить ссылку на ячейку масштабирования по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ScaleY  <br/> |
   
Чтобы получить ссылку на ячейку масштабирования по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**висровпринтпропертиес** <br/> |
|Индекс ячейки:  <br/> |**виспринтпропертиесскалэй** <br/> |
   

