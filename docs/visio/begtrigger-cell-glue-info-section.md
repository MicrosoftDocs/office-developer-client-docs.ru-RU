---
title: BegTrigger Cell (Glue Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Содержит формулу триггера, созданную приложением, которая определяет, следует ли перемещать точки начала одно d фигуры для поддержания соединения с другой фигурой.
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437954"
---
# <a name="begtrigger-cell-glue-info-section"></a>BegTrigger Cell (Glue Info Section)

Содержит формулу триггера, созданную приложением, которая определяет, следует ли перемещать точки начала одно d фигуры для поддержания соединения с другой фигурой.
  
## <a name="remarks"></a>Примечания

При приклеить одномерную фигуру к другой фигуре с помощью динамического приклейки приложение создает формулу, которая ссылается на ячейку EventXFMod другой фигуры. При смене фигуры Visio пересчитывает все формулы, которые ссылаются на ее ячейку EventXFMod, включая формулу в ячейке BegTrigger. Другие формулы для 1-D фигуры ссылаются на ячейку BegTrigger и перемещают точки начала 1-D фигуры или при необходимости изменяют фигуру.
  
Чтобы получить ссылку на ячейку BegTrigger по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BegTrigger  <br/> |
   
Чтобы получить ссылку на ячейку BegTrigger по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGroup** <br/> |
| Индекс ячейки:  <br/> |**visBegTrigger** <br/> |
   

