---
title: Ячейка Default (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Определяет гиперссылку по умолчанию для фигуры или страницы. Задайте значение в этой ячейке значение TRUE, чтобы установить гиперссылки по умолчанию.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813570"
---
# <a name="default-cell-hyperlinks-section"></a>Ячейка Default (раздел "Гиперссылки")

Определяет гиперссылку по умолчанию для фигуры или страницы. Задайте значение в этой ячейке значение TRUE, чтобы установить гиперссылки по умолчанию.
  
## <a name="remarks"></a>Замечания

Также можно настроить гиперссылку по умолчанию, выделение фигуры, щелкнув вкладку **Вставка** **гиперссылки** , выбрав гиперссылки и затем выбрав **по умолчанию**. Ссылка на по умолчанию отображается полужирным шрифтом.
  
Для получения ссылки на ячейки по умолчанию по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |Гиперссылки. *Имя* . Значение по умолчанию где гиперссылки. *Имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки по умолчанию по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkDefault** <br/> |
   
