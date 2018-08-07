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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807255"
---
# <a name="funcfib"></a>FuncFib

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательских функция, которая вычисляет n-й Фибоначчи. При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Параметры

 _pxN_ (**LPXLOPER12**)
  
Значение N, для которого необходим n-й Фибоначчи.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

(**xltypeNum LPXLOPER12** в случае успешного выполнения или **xltypeErr** в противном случае —) 
  
N-й Фибоначчи.
  
## <a name="remarks"></a>Замечания

Функция использует определен в блоке функции как возвращаемое значение **XLOPER12**статическую переменную. Это не потокобезопасными, и поэтому эта функция и любая другая функция, которая использует эту стратегию для возврата **XLOPER**или **XLOPER12**, не должны быть зарегистрированы как потокобезопасными, начиная с версии Excel 2007.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции из универсальной библиотеки DLL](functions-in-the-generic-dll.md)

