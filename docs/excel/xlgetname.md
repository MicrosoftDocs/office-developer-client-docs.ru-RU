---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- Функция xlgetname [excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 350ae99baf088a36fa3e1159caa1805cdd623276
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430590"
---
# <a name="xlgetname"></a>xlGetName

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает полный путь и имя файла DLL в виде строки.
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает путь и имя файла (**xltypeStr).** 
  
## <a name="example"></a>Пример

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>См. также

- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

