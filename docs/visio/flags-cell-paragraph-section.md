---
title: Ячейка Flags (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Указывает, будет ли направление — слева направо или справа налево.
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813764"
---
# <a name="flags-cell-paragraph-section"></a>Ячейка Flags (раздел "Абзац")

Указывает, будет ли направление — слева направо или справа налево.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Направление текста слева направо (по умолчанию).  <br/> |
|1  <br/> |Направление текста справа налево.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение в этой ячейке соответствует параметру **направление** на вкладке **абзаца** в диалоговое окно " **Text** " (на вкладке **Главная** щелкните стрелку **шрифта** ), которая появляется только в том случае, если язык, который используется сложных сценариев текст был добавлено в диалоговом окне **Языковые параметры Microsoft Office** . (Нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы**, нажмите кнопку **Microsoft Office**, средства **Microsoft Office**и затем выберите **Языковые параметры Microsoft Office**.) 
  
Для получения ссылки на ячейки флаги по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Para.Flags [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки флаги по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visFlags** <br/> |
   
