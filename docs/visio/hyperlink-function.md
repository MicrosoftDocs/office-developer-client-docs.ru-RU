---
title: Функция HYPERLINK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Переходит на указанный адрес, который может быть путем к файлу, UNC или URL-адресу.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329948"
---
# <a name="hyperlink-function"></a>Функция HYPERLINK

Переходит на указанный адрес, который может быть путем к файлу, UNC или URL-адресу.
  
## <a name="syntax"></a>Синтаксис

HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Обязательно  <br/> |**Строка** <br/> |Полный или относительный путь.  <br/> |
| _subaddress_ <br/> |Необязательна  <br/> |**Строка** <br/> |Указывает расположение в адресе для ссылки. Например, если адрес — это файл Microsoft Visio, подадрес может быть именем страницы; если файл Microsoft Excel, подадрес может быть листа или диапазона в пределах листа; Если URL-адрес htmL-страницы, подадрес может быть привязкой.  <br/> |
| _extrainfo_ <br/> |Необязательна  <br/> |**Строка** <br/> |Передает сведения, используемые при разрешении URL-адреса, например координаты карты изображения.  <br/> |
| _window_ <br/> |Необязательный  <br/> |**Логический** <br/> |Указывает, открывается ли гиперссылка в новом окне. Значение по умолчанию — FALSE.  <br/> |
| _frame_ <br/> |Необязательна  <br/> |**Строка** <br/> | Указывает имя кадра, на который необходимо нацелить, когда Visio открывается как активный документ в браузере ActiveX, например Microsoft Internet Explorer 3.0 или более поздней. Значение по умолчанию — пустая строка.  <br/> |
   
## <a name="remarks"></a>Примечания

Если в документе нет базового пути, Visio переходит по этому пути. Если документ не был сохранен, гиперссылка не будет запределена. 
  
Относительные пути основаны  на базовом поле гиперссылки, указанном в диалоговом **окне "Свойства Visio".** 
  
Вы можете использовать функцию GOTOPAGE для перемещения на страницы документа. 
  
## <a name="example-1"></a>Пример 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Пример 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Пример 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Пример 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

