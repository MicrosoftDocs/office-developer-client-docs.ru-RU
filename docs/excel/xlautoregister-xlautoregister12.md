---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- функция xlautoregister [Excel 2007]
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
  
Excel вызывает функцию [xlAutoRegister](xlautoregister-xlautoregister12.md) всякий раз, когда вызов был сделан в регистр функции XLM **или** функцию XPI, эквивалентную [XlfRegister](xlfregister-form-1.md)C, при этом отсутствуют типы возвращаемой и аргументированной функции. Она позволяет XLL искать внутренние списки экспортных функций и команд для регистрации функции с указанными типами аргументов и возврата.
  
Начиная с Excel 2007 г., Excel вызывает функцию **xlAutoRegister12** в предпочтение функции **xlAutoRegister,** если она экспортируется XLL. 
  
Excel XLL не требуется для реализации и экспорта этих функций.
  
> [!NOTE]
> Если **xlAutoRegister** /  **xlAutoRegister12** пытается зарегистрировать функцию, не поставляя типы аргументов и возврата, возникает цикл повторного вызова, который в конечном итоге переполниет стек вызовов и сбои Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameters

 _pxName_ **(xltypeStr)**
  
Имя зарегистрированной функции XLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция должна возвращать результат попытки зарегистрировать _pxName_ функции XLL с помощью **функции xlfRegister.** Если указанная функция не является экспортом XLL, она должна вернуть **#VALUE!** ошибка, **или NULL,** Excel будет интерпретироваться **в #VALUE!.**
  
## <a name="remarks"></a>Примечания

Реализация **xlAutoRegister** должна выполнять нечувствительный поиск через внутренние списки функций и команд XLL, экспортированных в поисках совпадения с переданным именем. Если функция или команда найдена, **xlAutoRegister** должен попытаться зарегистрировать ее с помощью функции **xlfRegister,** чтобы предоставить строку, которая Excel типам возврата и аргументов функции, а также любые другие необходимые сведения о функции. Затем он должен вернуться в Excel все **вызовы xlfRegister** возвращены. Если функция была успешно зарегистрирована, **xlfRegister** возвращает **значение xltypeNum,** содержащее ID регистра функции. 
  
### <a name="example"></a>Пример

Пример реализации этой  `SAMPLES\EXAMPLE\EXAMPLE.C` функции см. в файле. 
  
## <a name="see-also"></a>См. также



[РЕГИСТРАЦИЯ](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

