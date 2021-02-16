---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- функция funcfib [excel 2007]
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
  
Пример определяемой пользователем функции таблицы, которая вычисляет Nth Fibonacci number. При загрузке GENERIC.xll она регистрирует эту функцию, чтобы ее можно было вызвано с помощью таблицы.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Параметры

 _pxN_ (**LPXLOPER12)**
  
Значение N, для которого требуется N-й номер Fibonacci.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

(**xltypeNum LPXLOPER12,** если успешно или **xltypeErr в противном случае)** 
  
N-й номер Fibonacci.
  
## <a name="remarks"></a>Примечания

Функция использует статическую переменную, определяемую в блоке функции, в качестве возвращаемой **переменной XLOPER12.** Это не потокобезопасная функция, поэтому эта функция и любая функция листа, использующая эту стратегию для возврата S или **XLOPER12 XLOPER12,** не должна быть зарегистрирована как потокобезопасная, начиная с Excel 2007. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

