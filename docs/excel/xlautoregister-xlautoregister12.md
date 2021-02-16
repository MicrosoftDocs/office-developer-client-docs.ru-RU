---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Функция xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421167"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Excel вызывает функцию [xlAutoRegister](xlautoregister-xlautoregister12.md) всякий раз, когда был выполнен вызов функции XLM **REGISTER** или функции [XLFRegister,](xlfregister-form-1.md)эквивалентной API C, при этом отсутствуют типы возвращаемого и аргументного аргументов функции. Он позволяет XLL искать внутренние списки экспортных функций и команд для регистрации функции с указанным аргументом и типами возврата.
  
Начиная с Excel 2007, Excel вызывает функцию **xlAutoRegister12** в предпочтение функции **xlAutoRegister,** если она экспортирована с помощью XLL. 
  
Excel не требует XLL для реализации и экспорта этих функций.
  
> [!NOTE]
> Если **xlAutoRegister** /  **xlAutoRegister12** пытается зарегистрировать функцию без аргумента и возвращаемого типа, возникает цикл рекурсивного вызова, который в конечном итоге переполнен стек вызовов и сбой Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Параметры

 _pxName_ (**xltypeStr)**
  
Имя зарегистрированной функции XLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция должна возвращать результат попытки зарегистрировать _pxName_ функции XLL с помощью **функции xlfRegister.** Если указанная функция не является экспортом XLL, она должна вернуть **#VALUE!** ошибка или **NULL,** которые Excel интерпретирует **при #VALUE!**.
  
## <a name="remarks"></a>Примечания

Реализация **xlAutoRegister** должна выполнять поиск с помощью внутренних списков функций xLL и команд, экспортированных в поиск совпадения с переданным именем. Если функция или команда найдена, **xlAutoRegister** должен попытаться зарегистрировать ее с помощью функции **xlfRegister,** чтобы предоставить строку, которая сообщает Excel типы возвращаемого и аргумента функции, а также любые другие необходимые сведения о функции. Затем он должен возвращаться в Excel независимо от того, что **возвращено вызовом xlfRegister.** Если функция успешно зарегистрирована, **xlfRegister** возвращает **значение xltypeNum,** содержащее ИД регистрации функции. 
  
### <a name="example"></a>Пример

Пример реализации этой  `SAMPLES\EXAMPLE\EXAMPLE.C` функции см. в файле. 
  
## <a name="see-also"></a>См. также



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

