---
title: Prompt Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Указывает описательный или пояснительный текст, который отображается в виде подсказки при приостановке указателя мыши над значением в окне Данные фигуры.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405487"
---
# <a name="prompt-cell-shape-data-section"></a>Prompt Cell (Shape Data Section)

Указывает описательный или пояснительный текст, который отображается в виде подсказки при приостановке указателя мыши над значением в окне **данные фигуры** . 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку приглашения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Установите.  *Name (имя* ). Подсказка, где *Name* — имя строки  <br/> |
   
Чтобы получить ссылку на ячейку приглашения по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**виссектионпроп** <br/> |
| Индекс строки:  <br/> |**висровпроп +** *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**вискустпропспромпт** <br/> |
   

