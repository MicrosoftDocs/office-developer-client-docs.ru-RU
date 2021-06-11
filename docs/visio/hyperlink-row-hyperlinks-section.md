---
title: Hyperlink Row (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылки для каждой гиперссылки.
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329906"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Hyperlink Row (Hyperlinks Section)

Содержит сведения для одной гиперссылки, связанной с фигурой. Фигура будет содержать одну строку гиперссылки для каждой гиперссылки.
  
Строки гиперссылки называются Hyperlink. *имя*  и содержать следующие ячейки. Дополнительные сведения см. в конкретных разделах ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[Описание](description-cell-hyperlinks-section.md) <br/> |Текстовая строка для гиперссылки.  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |URL-адрес, имя файла MS-DOS или путь к которому можно перейти.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Расположение в целевом документе для ссылки.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Строка, которая передает сведения, которые будут использоваться для решения URL-адреса.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Имя кадра для целевого Microsoft Office Visio в качестве активного документа в ActiveX контейнере. По умолчанию это пустая строка.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Определяет порядок гиперссылки по мере их появления в меню ярлыков.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Указывает, следует ли открывать гиперссылку в новом окне. Если TRUE, откроет связанную страницу, документ или веб-сайт в новом окне. По умолчанию значение FALSE.  <br/> |
|[По умолчанию](default-cell-hyperlinks-section.md) <br/> |Гиперссылка по умолчанию для формы или страницы.  <br/> |
|[Невидимый](invisible-cell-hyperlinks-section.md) <br/> |Указывает, отображается ли гиперссылка в меню ярлыка.  <br/> |
   
## <a name="remarks"></a>Примечания

 Можно добавить как можно больше гиперссылки.  *Строки*  имен по мере необходимости назначьте значимые имена строкам и установите значения ячейки. Чтобы добавить гиперссылки в существующий раздел Гиперссылки, щелкните правой кнопкой мыши строку и нажмите **кнопку Вставить строку** в меню ярлыка. 
  
Вы можете ссылаться на эти ячейки по имени строки, которое отображается в окне ShapeSheet в красном тексте. Назначение значимых имен гиперссылке. *строки*  имен, щелкните строку, а затем введите имя, такое как  *Маркетинг,*  например, чтобы создать имя строки Hyperlink.Marketing. Затем можно ссылаться на ячейку Description с помощью Hyperlink.Marketing.Description. 
  
Имя строки, которое вы вводите, должно быть уникальным в разделе.
  

