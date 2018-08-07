---
title: Ячейка Visible (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Указывает, отображаются на странице документа ли фигур, относящегося к слою.
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815140"
---
# <a name="visible-cell-layers-section"></a>Ячейка Visible (раздел "Слои")

Указывает, отображаются на странице документа ли фигур, относящегося к слою.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Видны фигур.  <br/> |
|FALSE  <br/> |Фигуры являются скрытыми.  <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует параметру **Visible** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer** ). 
  
Для получения ссылки на ячейки видимым по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Layers.Visible [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки видимым по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visLayerVisible** <br/> |
   

