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
  
Строки гиперссылки называются гиперссылкой. *имя*  и содержать следующие ячейки. Дополнительные сведения см. в определенных темах о ячейках. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[Описание](description-cell-hyperlinks-section.md) <br/> |Текстовая строка для гиперссылки.  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |URL-адрес, имя файла MS-DOS или UNC-путь, к которому необходимо перейти.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Расположение в целевом документе, к который необходимо связать.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Строка, которая передает сведения для использования при разрешении URL-адреса.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Имя кадра для цели, Microsoft Office Visio открыт как активный документ в ActiveX контейнере. Значение по умолчанию — пустая строка.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Определяет порядок гиперссылки по мере их появления в ярлыковом меню.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Указывает, следует ли открывать гиперссылки в новом окне. Если имеется true, в новом окне откроется связанная страница, документ или веб-сайт. Значение по умолчанию — FALSE.  <br/> |
|[По умолчанию](default-cell-hyperlinks-section.md) <br/> |Гиперссылка по умолчанию для фигуры или страницы.  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Указывает, отображается ли гиперссылка в ярлыковом меню.  <br/> |
   
## <a name="remarks"></a>Примечания

 Можно добавить как можно больше гиперссылки.  *назначать*  строкам имена по мере необходимости, назначать осмысленные имена строкам и задавать значения ячеей. Чтобы добавить гиперссылки в существующий раздел "Гиперссылки", щелкните правой кнопкой мыши строку и выберите пункт **"Вставка** строки" в ярлыковом меню. 
  
Вы можете ссылаться на эти ячейки по имени строки, которое отображается в окне таблицы фигур в красном тексте. Назначение осмысленных имен гиперссылке. *щелкните*  строку имени, а затем введите имя, например  *"Маркетинг",*  чтобы создать имя строки Hyperlink.Marketing. Затем можно ссылаться на ячейку Description с помощью Hyperlink.Marketing.Description. 
  
Введите уникальное имя строки в разделе.
  

