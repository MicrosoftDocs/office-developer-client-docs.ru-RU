---
title: Label Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Указывает метку, которая отображается пользователям в окне Shape Data. Метка состоит из символов альфа-цифр, включая символ underscore (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420180"
---
# <a name="label-cell-shape-data-section"></a>Label Cell (Shape Data Section)

Указывает метку, которая отображается пользователям в **окне Shape Data.** Метка состоит из символов альфа-цифр, включая символ underscore (_). 
  
## <a name="remarks"></a>Примечания

Приложение автоматически заключит строку Label в кавычках в ячейке, но кавычка не отображается в окне **Shape Data.** 
  
Если текст метки не найден, Visio отображает имя строки (Prop.Row) в **окне Shape Data.** 
  
Чтобы получить ссылку на ячейку Label по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Prop. *Name*  . Метка, на которой проп.  *Имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Label по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionProp** <br/> |
|Индекс строки:  <br/> |**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visCustPropsLabel** <br/> |
   

