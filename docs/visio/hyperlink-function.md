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
description: Переходит по указанному адресу, который может быть URL-адресом файла, UNC-пути или URL-адреса.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329948"
---
# <a name="hyperlink-function"></a>Функция HYPERLINK

Переходит по указанному адресу, который может быть URL-адресом файла, UNC-пути или URL-адреса.
  
## <a name="syntax"></a>Синтаксис

Гиперссылка ("* ** адрес* * *" [, "* ** подадрес* * *", "* * *extrainfo* * *", * * *окно* * *, "* * *Frame* * *"]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Обязательный  <br/> |**String** <br/> |Полный или относительный путь.  <br/> |
| _subaddress_ <br/> |Необязательна  <br/> |**String** <br/> |Указывает расположение для ссылки в адресе. Например, если Address — это файл Microsoft Visio, подадрес может быть именем страницы; Если файл Microsoft Excel, подадрес может быть листом или диапазоном на листе; Если URL-адрес HTML-страницы, подадрес может быть привязкой.  <br/> |
| _ExtraInfo_ <br/> |Необязательна  <br/> |**String** <br/> |Передает сведения, используемые при разрешении URL-адреса, такие как координаты карты ссылок.  <br/> |
| _окно_ <br/> |Необязательный  <br/> |**Логический** <br/> |Указывает, следует ли открыть гиперссылку в новом окне. Значение по умолчанию — FALSE.  <br/> |
| _кадры_ <br/> |Необязательна  <br/> |**String** <br/> | Задает имя конечного кадра при открытии Visio в качестве активного документа в браузере ActiveX, например Microsoft Internet Explorer 3,0 или более поздней версии. Значение по умолчанию — пустая строка.  <br/> |
   
## <a name="remarks"></a>Примечания

Если у документа нет базового пути, Visio переходит в соответствии с путем к документу. Если документ не был сохранен, гиперссылка не определена. 
  
Относительные пути зависят от поля **базы гиперссылки** , указанного в диалоговом окне " **свойства Visio** ". 
  
С помощью функции GOTOPAGE можно переходить к страницам документа. 
  
## <a name="example-1"></a>Пример 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Пример 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Пример 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Пример 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

