---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310292"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция обратного вызова, которая должна быть реализована и экспортирована каждым действительным XLL. Функция **xlAutoOpen** рекомендуется использовать для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и т. д. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Microsoft Excel вызывает **xlAutoOpen** всякий раз при активации XLL. XLL-модуль активируется в следующих ситуациях: 
  
- В начале сеанса Excel, если он был активен в последнем сеансе Excel, который нормально завершил работу.
    
- При загрузке во время сеанса Excel.
    
- XLL можно загрузить несколькими способами:
    
- Выбрав команду **Открыть** в меню **файл** (где версия Excel поддерживает этот метод загрузки XLL-модулей). 
    
- С помощью диспетчера надстроек.
    
- Из другого XLL, который вызывает [xlfRegister](xlfregister-form-1.md) с именем этой библиотеки DLL в качестве единственного аргумента. 
    
- На листе макросов XLM, который вызывает [Register](xlfregister-form-1.md) с именем этой библиотеки DLL в качестве единственного аргумента. 
    
- Если надстройка отключена и повторно активирована во время сеанса Excel, эта функция вызывается при повторной активации.
    
### <a name="example"></a>Пример

Просмотрите файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C`, в частности, примеры реализации этой функции.
  
## <a name="see-also"></a>См. также



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

