---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- функция funcfib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423673"
---
# <a name="funcfib"></a>FuncFib

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример функции таблицы, определяемой пользователем, которая вычисляет номер Nth Fibonacci. При загрузке GENERIC.xll она регистрирует эту функцию, чтобы она была вызвана из таблицы.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parameters

 _pxN_ **(LPXLOPER12)**
  
Значение N, для которого требуется номер Nth Fibonacci.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

(**xltypeNum LPXLOPER12** при успешном или **xltypeErr** в противном случае) 
  
Номер Nth Fibonacci.
  
## <a name="remarks"></a>Примечания

Функция использует статическую переменную, определяемую в блоке функций в качестве возвращаемой **величины XLOPER12.** Это не безопасно, поэтому эта функция, и любая функция таблицы, использующая эту стратегию для возврата **XLOPER** s или **XLOPER12** s, не должна быть зарегистрирована в качестве безопасной для потока начиная с Excel 2007 г.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

