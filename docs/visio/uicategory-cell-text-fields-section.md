---
title: UICategory Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Определяет категорию вставленного поля в более ранних версиях Visio, чем Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434027"
---
# <a name="uicategory-cell-text-fields-section"></a>UICategory Cell (Text Fields Section)

Определяет категорию вставленного поля в более ранних версиях Visio, чем Visio 2000.
  
## <a name="remarks"></a>Примечания

Эта ячейка не отображается в окне таблицы свойств фигуры. Используйте эту ячейку, если вам нужно разобраться с проблемами обратной связи, например, сохранив документ Visio версии 2000 в формате файлов Visio версии 5,0.
  
Чтобы получить ссылку на ячейку UICategory по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Fields. Уикат [ *i* ], где *i* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку UICategory по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**Виссектионтекстфиелд** <br/> |
| Индекс строки:  <br/> |**висровфиелд** +  *i* , где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Висфиелдуикатегори** <br/> |
   

