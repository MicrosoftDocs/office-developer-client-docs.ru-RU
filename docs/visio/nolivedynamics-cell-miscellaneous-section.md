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
description: Определяет, будет ли фигура динамически изменять размер или поворачиваться при управлении ею.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421482"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>NoLiveDynamics Cell (Miscellaneous Section)

Определяет, будет ли фигура динамически изменять размер или поворачиваться при управлении ею.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Не обновляйте фигуру динамически при управлении ею.  <br/> |
| FALSE  <br/> | Динамическое обновление фигуры во время управления ею.  <br/> |
   
## <a name="remarks"></a>Примечания

При изменении размера или повороте двухмерной (2-D) фигуры без динамического Dynamics отображается поле выбора. Если фигура является одномерным (1-D), визуальная обратная связь основывается на значении в ячейке DynFeedback.
  
Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoLiveDynamics  <br/> |
   
Чтобы получить ссылку на ячейку NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровмиск** <br/> |
| Индекс ячейки:  <br/> |**Висноливединамикс** <br/> |
   

