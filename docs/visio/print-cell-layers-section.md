---
title: Ячейка Print (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Указывает, можно ли печатать фигур, относящегося к слою.
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814483"
---
# <a name="print-cell-layers-section"></a>Ячейка Print (раздел "Слои")

Указывает, можно ли печатать фигур, относящегося к слою.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Можно распечатать фигур.  <br/> |
|FALSE  <br/> |Не удается напечатать фигур.  <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение с помощью параметра **печати** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).
  
Для получения ссылки на ячейки Print по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Layers.Print [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки Print по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionLayer** <br/> |
|Индекс строки:  <br/> |**visRowLayer** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visDocPreviewScope** <br/> |
   

