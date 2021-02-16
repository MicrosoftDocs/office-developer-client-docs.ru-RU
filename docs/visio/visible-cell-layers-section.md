---
title: Visible Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Указывает, видны ли фигуры уровня на странице рисования.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405452"
---
# <a name="visible-cell-layers-section"></a>Visible Cell (Layers Section)

Указывает, видны ли фигуры уровня на странице рисования.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Фигуры видны.  <br/> |
|FALSE  <br/> |Фигуры скрыты.  <br/> |
   
## <a name="remarks"></a>Примечания

Эта ячейка соответствует параметру **Visible** в диалоговом **окне** "Свойства  слоя" (на вкладке "Главная" в группе редактирования щелкните "Слои" и выберите "Свойства **уровня").**   
  
Чтобы получить ссылку на ячейку Visible по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Layers.Visible[ *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Visible по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer**  +   *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visLayerVisible** <br/> |
   

