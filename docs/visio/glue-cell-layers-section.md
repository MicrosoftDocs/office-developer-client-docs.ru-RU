---
title: Ячейка связывающих (слои раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Указывает, может быть связан фигур, относящегося к слою.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813848"
---
# <a name="glue-cell-layers-section"></a>Ячейка связывающих (слои раздел)

Указывает, может быть связан фигур, относящегося к слою.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Связывающих включена.  <br/> |
|FALSE  <br/> |Связывающих отключено.  <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует параметру **связывающих** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer** ). 
  
Для получения ссылки на ячейки связывающих по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Layers.Glue [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки связывающих по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visLayerGlue** <br/> |
   
