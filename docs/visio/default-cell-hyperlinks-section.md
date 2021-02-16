---
title: Default Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Определяет гиперссылки по умолчанию для фигуры или страницы. Установите для этой ячейки значение TRUE, чтобы установить гиперссылки по умолчанию.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434356"
---
# <a name="default-cell-hyperlinks-section"></a>Default Cell (Hyperlinks Section)

Определяет гиперссылки по умолчанию для фигуры или страницы. Установите для этой ячейки значение TRUE, чтобы установить гиперссылки по умолчанию.
  
## <a name="remarks"></a>Примечания

Вы также можете установить гиперссылки по умолчанию, выбрав  фигуру, щелкнув "Гиперссылка" на вкладке "Вставка", выбрав гиперссылки и выбрав "По **умолчанию".**  Гиперссылка по умолчанию отображается полужирным шрифтом.
  
Чтобы получить ссылку на ячейку Default по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Гиперссылка. *Name*  . По умолчанию, где гиперссылка. *Имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Default по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkDefault** <br/> |
   

