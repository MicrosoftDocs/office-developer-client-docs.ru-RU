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
description: Переходит на указанный адрес, который может быть файлом, unC или URL-адресом.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329948"
---
# <a name="hyperlink-function"></a>Функция HYPERLINK

Переходит на указанный адрес, который может быть файлом, unC или URL-адресом.
  
## <a name="syntax"></a>Синтаксис

HYPERLINK(" ** *адрес* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Обязательный  <br/> |**String** <br/> |Полный путь или относительный путь.  <br/> |
| _subaddress_ <br/> |Необязательный  <br/> |**String** <br/> |Указывает расположение в адресе для ссылки на. Например, если адрес — это файл microsoft Visio, подадрес может быть именем страницы; если файл Microsoft Excel, подадрест может быть таблицой или диапазоном в пределах таблицы; если URL-адрес страницы HTML, подадрес может быть якорем.  <br/> |
| _extrainfo_ <br/> |Необязательный  <br/> |**String** <br/> |Передает сведения, используемые при разрешении URL-адреса, например координаты карты изображений.  <br/> |
| _окно_ <br/> |Необязательный  <br/> |**Логический** <br/> |Указывает, открыта ли гиперссылка в новом окне. По умолчанию значение FALSE.  <br/> |
| _кадр_ <br/> |Необязательный  <br/> |**String** <br/> | Указывает имя кадра для цели, если Visio в качестве активного документа в браузере ActiveX, например Microsoft Internet Explorer 3.0 или более поздней. По умолчанию это пустая строка.  <br/> |
   
## <a name="remarks"></a>Примечания

Если документ не имеет базового пути, Visio перемещается по пути документа. Если документ не сохранен, гиперссылка не установлена. 
  
Относительные пути основаны на базовом поле **Hyperlink,** указанном **в диалоговом окне Visio свойства.** 
  
Вы можете использовать функцию GOTOPAGE для перемещения по страницам документа. 
  
## <a name="example-1"></a>Пример 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Пример 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Пример 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Пример 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

