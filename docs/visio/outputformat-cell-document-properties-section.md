---
title: Ячейка OutputFormat (раздел свойств документа)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Определяет формат выходных данных для рисунка. Страницы документа обычно форматирования для печати (по умолчанию); Тем не менее вы можете других форматов вывода.
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814321"
---
# <a name="outputformat-cell-document-properties-section"></a>Ячейка OutputFormat (раздел свойств документа)

Определяет формат выходных данных для рисунка. Страницы документа обычно форматирования для печати (по умолчанию); Тем не менее вы можете других форматов вывода.
  
|**Значение**|**Формат выходных данных**|
|:-----|:-----|
| 0  <br/> | Печать (по умолчанию)  <br/> |
| 1  <br/> | Слайд-шоу PowerPoint  <br/> |
| 2  <br/> | Выходные данные HTML или GIF  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку OutputFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | OutputFormat  <br/> |
   
Для получения ссылки на ячейки OutputFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowDoc** <br/> |
| Индекс ячейки:  <br/> |**visDocOutputFormat** <br/> |
   

