---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Функция xlAutoRegister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303950"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel вызывает [функцию xlAutoRegister](xlautoregister-xlautoregister12.md) при каждом вызове в **регистре**функции XLM или В эквивалентной функции C API [xlfRegister](xlfregister-form-1.md)с типами возвращаемых значения и аргументов функции, которую вы зарегистрировали. Он позволяет XLL выполнить поиск по внутренним спискам экспортированных функций и команд, чтобы зарегистрировать функцию с указанными аргументами и возвращаемыми типами.
  
Начиная с Excel 2007, Excel вызывает функцию **xlAutoRegister12** в предпочтение функции **xlAutoRegister** , если она экспортируется XLL. 
  
В Excel не требуется XLL для реализации и экспорта любой из этих функций.
  
> [!NOTE]
> Если **xlAutoRegister**/ **xlAutoRegister12** пытается зарегистрировать функцию, не предоставляя аргументы и типы возвращаемых данных, вызывается рекурсивный цикл вызова, который в конечном итоге переполняет стек вызовов и завершает работу Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Параметры

 _пкснаме_ (**кслтипестр**)
  
Имя регистрируемой функции XLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция должна возвращать результат попытки зарегистрировать функцию XLL _пкснаме_ с помощью функции **xlfRegister** . Если указанная функция не является одним из экспортируемых компонентов XLL, она должна возвращать **#VALUE!** ошибка или **значение NULL** , которое будет интерпретировано в приложении Excel на **#VALUE!**.
  
## <a name="remarks"></a>Замечания

Ваша реализация **xlAutoRegister** должна выполнять поиск с учетом регистра, используя внутренние списки функций и команд, которые она экспортирует, в поисках сравнения с переданным именем. Если функция или команда найдена, **xlAutoRegister** должна попытаться зарегистрировать ее, используя функцию **xlfRegister** , убедившись, что строка, указывающая на Excel, возвращает типы возвращаемого значения и аргументы функции, а также любые другие необходимые сведения о функции. Затем он должен вернуться в Excel, что бы возвращался вызов **xlfRegister** . Если функция была зарегистрирована успешно, **xlfRegister** возвращает значение **КСЛТИПЕНУМ** , содержащее идентификатор регистра функции. 
  
### <a name="example"></a>Пример

В этом файле `SAMPLES\EXAMPLE\EXAMPLE.C` представлен пример реализации этой функции. 
  
## <a name="see-also"></a>См. также



[РЕГИСТРАЦИЯ](xlfregister-form-1.md)
  
[Отмена регистрации](xlfunregister-form-1.md)

