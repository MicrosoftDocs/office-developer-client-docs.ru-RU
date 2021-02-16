---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- Функция xlautoopen [excel 2007]
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
  
Функция callback, которую необходимо реализовать и экспортировать с помощью каждой допустимой XLL. Функция **xlAutoOpen** — это рекомендуемое место для регистрации функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и других функций. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Microsoft Excel вызывает **xlAutoOpen** при активации XLL. XLL активируется в следующих ситуациях: 
  
- В начале сеанса Excel, если он был активен в последнем сеансе Excel, который завершился нормально.
    
- При загрузке во время сеанса Excel.
    
- XLL можно загрузить несколькими способами:
    
- Выбрав пункт **"Открыть** в **меню "Файл"** (где версия Excel поддерживает этот метод загрузки XLL). 
    
- С помощью диспетчера надстроек.
    
- Из другой XLL, которая вызывает [xlfRegister](xlfregister-form-1.md) с именем этой DLL в качестве единственным аргументом. 
    
- Из листа макроса XLM, который вызывает [REGISTER](xlfregister-form-1.md) с именем этой DLL в качестве единственным аргументом. 
    
- Если надстройка деактивирована и активирована повторно во время сеанса Excel, эта функция будет вызвана при повторной активности.
    
### <a name="example"></a>Пример

См. файлы  `SAMPLES\EXAMPLE\EXAMPLE.C`  `SAMPLES\GENERIC\GENERIC.C` и примеры реализации этой функции.
  
## <a name="see-also"></a>См. также



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

