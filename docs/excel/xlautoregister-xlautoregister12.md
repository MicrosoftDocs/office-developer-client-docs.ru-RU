---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- функция xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807338"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel вызывает [функцию xlAutoRegister](xlautoregister-xlautoregister12.md) при вызова функции XLM, **Регистрация**или эквивалентный интерфейса API для C [xlfRegister функции](xlfregister-form-1.md), с помощью типов возврата и аргумент функции регистрации отсутствует. Это позволяет XLL-Модулей для поиска его внутренней списки экспортированных функций и команды, чтобы зарегистрировать функцию в аргументе и возвращаемые типы указан.
  
Начиная с версии Excel 2007, Excel вызывает функцию **xlAutoRegister12** вместо функции **xlAutoRegister** при экспорте с XLL. 
  
Excel не требуется XLL внедрение и экспортировать любой из этих функций.
  
> [!NOTE]
> Если **xlAutoRegister**/ **xlAutoRegister12** пытается зарегистрировать функцию без указания аргументов и возвращаемых типов, вызывающий рекурсивный цикл возникает которого со временем переполнение стека вызовов и завершает работу Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameters

 _pxName_ (**xltypeStr**)
  
Имя функции XLL, который требуется зарегистрировать.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция должна вернуть результат попытки для регистрации функции XLL _pxName_ , с помощью функции **xlfRegister** . Если указанная функция не является одним из экспортируемые, он должен возвращать **#VALUE!** сообщение об ошибке, или **значение NULL,** что Excel будет интерпретировать в **#VALUE!**.
  
## <a name="remarks"></a>Замечания

Реализация **xlAutoRegister** следует выполнять поиск без учета регистра через вашей XLL внутренних списков функций и команд, экспортируется совпадение с именем переданное. При обнаружении функции или команды, **xlAutoRegister** производится попытка регистрации с помощью функции **xlfRegister** , сохраняя для предоставления строка, которая указывает типы возврата и аргумент функции, а также любые другие необходимые Excel сведения о функции. Он должен возвращать в Excel независимо от существующих в **xlfRegister** , возвращенного. Если функция успешно зарегистрирована, **xlfRegister** возвращает значение **xltypeNum** , содержащее идентификатор регистрации функции. 
  
### <a name="example"></a>Пример

Просмотрите файл `SAMPLES\EXAMPLE\EXAMPLE.C` пример внедрения этой функции. 
  
## <a name="see-also"></a>См. также



[РЕГИСТРАЦИЯ](xlfregister-form-1.md)
  
[ОТМЕНА РЕГИСТРАЦИИ](xlfunregister-form-1.md)

