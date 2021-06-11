---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlautoopen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406649"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция вызова, которая должна быть реализована и экспортироваться каждым допустимым XLL. Функция **xlAutoOpen** — это рекомендуемое место для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и так далее. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Microsoft Excel **xlAutoOpen при** активации XLL. XLL активируется в следующих ситуациях: 
  
- В начале сеанса Excel, если он был активен в последнем сеансе Excel, завершившейся нормально.
    
- При загрузке во время Excel сеанса.
    
- XLL можно загрузить несколькими способами:
    
- Выбрав Open **в** меню **File** (где версия Excel поддерживает этот метод загрузки XLLs). 
    
- С помощью диспетчера надстроек.
    
- Из другого XLL, который [вызывает xlfRegister](xlfregister-form-1.md) с именем этого DLL в качестве единственным аргументом. 
    
- С макрос листа XLM, который вызывает [REGISTER](xlfregister-form-1.md) с именем этого DLL в качестве единственным аргументом. 
    
- Если надстройка отключена и активирована во время сеанса Excel, эта функция будет активирована.
    
### <a name="example"></a>Пример

Просмотр файлов  `SAMPLES\EXAMPLE\EXAMPLE.C`  `SAMPLES\GENERIC\GENERIC.C` и, например, реализаций этой функции.
  
## <a name="see-also"></a>См. также



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

