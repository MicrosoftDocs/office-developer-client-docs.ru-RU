---
title: Ячейка Prompt (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Задает описательный или управляющий текст, который отображается в виде подсказки при наведении курсора на значение в окне данных фигуры.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814486"
---
# <a name="prompt-cell-shape-data-section"></a>Ячейка Prompt (раздел "Данные фигуры")

Задает описательный или управляющий текст, который отображается в виде подсказки при наведении курсора на значение в окне **Данных фигуры** . 
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки приглашениями по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Свойства.  *Имя* . Запрос, где *имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки приглашениями по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionProp** <br/> |
| Индекс строки:  <br/> |**visRowProp +** *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCustPropsPrompt** <br/> |
   

