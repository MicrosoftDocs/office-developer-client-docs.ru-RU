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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807257"
---
# <a name="func1"></a>Func1

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской функции показано возвращение статического строковое значение. При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parameters

 _точек_ (**LPXLOPER**)
  
Этот аргумент игнорируется и используется только для запуска Microsoft Excel для вызова функции.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

 **LPXLOPER12**: всегда строка «Func1»
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

