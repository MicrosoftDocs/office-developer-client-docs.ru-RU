---
title: Lock Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Указывает, заблокированы ли выбранные или редактируемые фигуры уровня.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438829"
---
# <a name="lock-cell-layers-section"></a>Lock Cell (Layers Section)

Указывает, заблокированы ли выбранные или редактируемые фигуры уровня.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Фигуры заблокированы.  <br/> |
|FALSE  <br/> |Фигуры не заблокированы.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить это  значение, выбрав "Блокировка" в  диалоговом  **окне** "Свойства уровня" (на вкладке "Главная" в группе редактирования щелкните "Слои" и выберите "Свойства **уровня").** 
  
Чтобы получить ссылку на ячейку Lock по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Locked[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Lock по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i,* *где i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visLayerLock** <br/> |
   

