---
title: LocalizeMerge Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Определяет, локализуются ли формы при их копировании в документы.
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344580"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>LocalizeMerge Cell (Miscellaneous Section)

Определяет, локализуются ли формы при их копировании в документы.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Локализация фигуры на языке целевого документа.  <br/> |
| FALSE  <br/> | Не следует локализовать фигуру на основе языка конечного документа (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку LocalizeMerge по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LocalizeMerge  <br/> |
   
Чтобы получить ссылку на ячейку LocalizeMerge по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровмиск** <br/> |
| Индекс ячейки:  <br/> |**Висобжлокализемерже** <br/> |
   

