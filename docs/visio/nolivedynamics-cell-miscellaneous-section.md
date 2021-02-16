---
title: NoLiveDynamics Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Определяет, динамически ли размер фигуры меняется или поворачивается при ее обработке.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421482"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>NoLiveDynamics Cell (Miscellaneous Section)

Определяет, динамически ли размер фигуры меняется или поворачивается при ее обработке.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не обновляя фигуру динамически во время ее обработки.  <br/> |
| FALSE  <br/> | Динамическое обновление фигуры во время ее обработки.  <br/> |
   
## <a name="remarks"></a>Примечания

При вращающейся двумерной (двухмерной) фигуре без динамической динамики вы увидите поле выбора. Если фигура одномерная (одномерная), визуальная обратная связь зависит от значения ячейки DynFeedback.
  
Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoLiveDynamics  <br/> |
   
Чтобы получить ссылку на ячейку NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoLiveDynamics** <br/> |
   

