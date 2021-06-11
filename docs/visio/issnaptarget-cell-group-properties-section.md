---
title: IsSnapTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Определяет, имеете ли вы привязку к группе или к фигурам в группе.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421447"
---
# <a name="issnaptarget-cell-group-properties-section"></a>IsSnapTarget Cell (Group Properties Section)

Определяет, имеете ли вы привязку к группе или к фигурам в группе.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включить привязку к фигурам в группе.  <br/> |
|FALSE  <br/> |прикрепление только для группы.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это значение, выбрав  группу, щелкнув "Поведение" на вкладке **Разработчик,** а затем прикрепление в поле фигур членов. [](run-in-developer-mode-display-the-developer-tab.md) 
  
Чтобы получить ссылку на ячейку IsSnapTarget по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |IsSnapTarget  <br/> |
   
Чтобы получить ссылку на ячейку IsSnapTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupIsSnapTarget** <br/> |
   

