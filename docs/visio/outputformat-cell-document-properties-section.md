---
title: OutputFormat Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Определяет формат вывода для рисунка. Страницы документа обычно форматируются для печати (по умолчанию); Тем не менее, вы можете выбрать другие форматы вывода.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413887"
---
# <a name="outputformat-cell-document-properties-section"></a>OutputFormat Cell (Document Properties Section)

Определяет формат вывода для рисунка. Страницы документа обычно форматируются для печати (по умолчанию); Тем не менее, вы можете выбрать другие форматы вывода.
  
|**Значение**|**Формат вывода**|
|:-----|:-----|
| нуль  <br/> | Печать (по умолчанию)  <br/> |
| 1,1  <br/> | Показ слайдов PowerPoint  <br/> |
| 2  <br/> | Вывод HTML или GIF  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку OutputFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | OutputFormat  <br/> |
   
Чтобы получить ссылку на ячейку OutputFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровдок** <br/> |
| Индекс ячейки:  <br/> |**Висдокаутпутформат** <br/> |
   

