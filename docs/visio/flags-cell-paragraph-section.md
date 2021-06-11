---
title: Flags Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Указывает, находится ли текстовое направление слева направо или справа налево.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413117"
---
# <a name="flags-cell-paragraph-section"></a>Flags Cell (Paragraph Section)

Указывает, находится ли текстовое направление слева направо или справа налево.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Текстовое направление слева направо (по умолчанию).  <br/> |
|1  <br/> |Направление текста справа налево.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение в этой ячейке  соответствует параметру Direction на  вкладке **Абзац** в диалоговом окне Текст (на вкладке Home нажмите стрелку **Шрифта),** которая появляется только в том случае, если язык, использующий сложный текст скриптов, был добавлен в диалоговом окне **Microsoft Office Языковые** предпочтения.  (Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office Инструменты**, а затем **нажмите кнопку Microsoft Office Языковые предпочтения**.) 
  
Чтобы получить ссылку на ячейку Флаги по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Para.Flags[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку Флаги по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visFlags** <br/> |
   

