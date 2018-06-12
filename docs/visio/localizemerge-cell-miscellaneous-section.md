---
title: Ячейка LocalizeMerge (раздел Разное)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Определяет локализованных фигуры при копировании в документы.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814107"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Ячейка LocalizeMerge (раздел Разное)

Определяет локализованных фигуры при копировании в документы.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Локализация фигуры на языке конечного документа.  <br/> |
| FALSE  <br/> | Не локализуйте фигуры на основе языка целевого документа (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LocalizeMerge по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LocalizeMerge  <br/> |
   
Для получения ссылки на ячейки LocalizeMerge по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visObjLocalizeMerge** <br/> |
   

