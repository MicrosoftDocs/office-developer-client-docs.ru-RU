---
title: Ячейка VerticalAlign (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Определяет вертикальное выравнивание текста в блоке текста.
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815145"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Ячейка VerticalAlign (раздел "Формат текстового блока")

Определяет вертикальное выравнивание текста в блоке текста.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Вверх  <br/> |**visVertTop** <br/> |
| 1  <br/> | Промежуточное  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Bottom  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку VerticalAlign по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | VerticalAlign  <br/> |
   
Для получения ссылки на ячейки VerticalAlign по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

