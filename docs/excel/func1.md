---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- функция func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408917"
---
# <a name="func1"></a>Func1

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример определяемой пользователем функции таблицы демонстрирует возврат статического строки. При загрузке GENERIC.xll она регистрирует эту функцию, чтобы ее можно было вызвано с помощью таблицы.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Параметры

 _px_ (**LPXLOPER)**
  
Этот аргумент игнорируется и служит только для вызова функции в Microsoft Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **LPXLOPER12**: всегда строка "Func1"
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

