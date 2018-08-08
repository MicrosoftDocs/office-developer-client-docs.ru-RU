---
title: Ячейка Comment (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Содержит текст комментария в формате строки для фигуры.
ms.openlocfilehash: f5222836b29a26cc26ca8093576d0962f0592fae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813412"
---
# <a name="comment-cell-miscellaneous-section"></a>Ячейка Comment (раздел "Прочее")

Содержит текст комментария в формате строки для фигуры.
  
## <a name="remarks"></a>Замечания

Также можно добавить примечание, нажав кнопку **Создать примечание** на вкладке **Обзор** . 
  
Чтобы получить ссылку на ячейку комментария по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Comment  <br/> |
   
Для получения ссылки на ячейки комментарий по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowMisc** <br/> |
|Индекс ячейки:  <br/> |**visComment** <br/> |
   

