---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- функция fdialog [excel 2007], функция fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807252"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, демонстрируется создание UDD Excel Microsoft (пользовательские диалоговое окно "") в библиотеке DLL с помощью возможностей поле диалогового окна в C API. При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция всегда возвращает 1.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

