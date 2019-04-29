---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- Функция функфиб [Excel 2007]
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
  
Пример пользовательской функции листа, которая вычисляет n число Фибоначчи. Когда GENERIC. XLL загружается, она регистрирует эту функцию, чтобы ее можно было вызывать из листа.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Параметры

 _ПКСН_ (**LPXLOPER12**)
  
Значение N, для которого необходим n-й номер последовательности Фибоначчи.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

(**КСЛТИПЕНУМ LPXLOPER12** в случае успеха или **кслтипирр** ). 
  
Значение последовательности Фибоначчи (n).
  
## <a name="remarks"></a>Примечания

В функции используется статическая переменная, определенная в блоке функции в качестве возвращаемого значения **XLOPER12**. Это не является потокобезопасным, поэтому эта функция и любая функция листа, использующая эту стратегию для возврата **XLOPER**s или **XLOPER12**, не должны регистрироваться как безопасный для потоков, начиная с Excel 2007.
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

