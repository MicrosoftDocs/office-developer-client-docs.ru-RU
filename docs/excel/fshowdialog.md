---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- Функция fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433593"
---
# <a name="fshowdialog"></a>fShowDialog

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, которая загружает и отображает пример нативного диалоговое окно Windows. При загрузке GENERIC.xll создается пользовательское меню Generic, через которое можно получить доступ к этой команде.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает никаких параметров.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция возвращает нулевое значение, чтобы указать успешное завершение
  
## <a name="remarks"></a>Примечания

Чтобы отобразить диалоговое окно Windows, выполните следующие действия.
  
1. Получите основной лад Windows Microsoft Excel с помощью **GetHwnd.**
    
2. Подключите главное окно Excel с помощью **HookExcelWindow.**
    
3. Отобразите диалоговое окно с помощью **DialogBox.**
    
4. Отогнали главное окно Excel с помощью **UnhookExcelWindow.**
    
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

