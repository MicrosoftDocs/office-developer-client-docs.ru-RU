---
title: ScaleX Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Указывает процентное отношение увеличения страницы документа на странице принтера.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410212"
---
# <a name="scalex-cell-print-properties-section"></a>ScaleX Cell (Print Properties Section)

Указывает процентное отношение увеличения страницы документа на странице принтера.
  
## <a name="remarks"></a>Примечания

Это значение используется только в том случае, если ячейка onPage имеет значение FALSE. Ячейки ScaleX и Scale всегда имеют одинаковое значение, которое соответствует значению, указанному в параметре **изменить** на вкладке **Настройка печати** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **настройки страницы** ). 
  
Чтобы получить ссылку на ячейку ScaleX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ScaleX  <br/> |
   
Чтобы получить ссылку на ячейку ScaleX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровпринтпропертиес** <br/> |
|Индекс ячейки:  <br/> |**Виспринтпропертиесскалекс** <br/> |
   

