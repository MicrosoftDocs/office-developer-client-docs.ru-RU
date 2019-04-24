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
description: Определяет, привязана ли к группе или к фигурам в группе.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317901"
---
# <a name="issnaptarget-cell-group-properties-section"></a>IsSnapTarget Cell (Group Properties Section)

Определяет, привязана ли к группе или к фигурам в группе.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |РазРешите привязку к фигурам в группе.  <br/> |
|FALSE  <br/> |ПриКрепление только к группе.  <br/> |
   
## <a name="remarks"></a>Замечания

Вы также можете задать это значение, выбрав группу, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установив флажок **привязать к фигурам участника** . 
  
Чтобы получить ссылку на ячейку IsSnapTarget по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |IsSnapTarget  <br/> |
   
Чтобы получить ссылку на ячейку IsSnapTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровграуп** <br/> |
|Индекс ячейки:  <br/> |**Висграуписснаптаржет** <br/> |
   

