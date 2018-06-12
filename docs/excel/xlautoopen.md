---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- функция xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807334"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция обратного вызова, который должен быть реализован и экспортировать с любой допустимый XLL-модуль. Функция **xlAutoOpen** используется, рекомендуется откуда регистрация функций и команд XLL, инициализации структур данных, настройки пользовательского интерфейса и так далее. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Реализация этой функции необходимо вернуть 1 (**int**).
  
## <a name="remarks"></a>Замечания

Microsoft Excel вызывает **xlAutoOpen** при активации XLL. XLL активируется в следующих ситуациях: 
  
- В начале сеанса обмена Excel, если она была активна последнего сеанса Excel, нормально.
    
- Если загружена во время сеанса обмена Excel.
    
- XLL-модуль может быть загружена несколькими способами:
    
- Выбрав команду **Открыть** в меню **файл** (где версии Excel поддерживает этот метод загрузки XLL-модулей). 
    
- Использование диспетчера надстроек.
    
- Из другой XLL [xlfRegister](xlfregister-form-1.md) с именем Эта DLL-Библиотека, которая вызывает только в качестве аргумента. 
    
- Из таблицы макросов XLM, который вызывает [регистрации](xlfregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента. 
    
- Если надстройка отключена и повторно во время сеанса обмена Excel, эта функция вызывается для повторной активации.
    
### <a name="example"></a>Пример

Файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C`и пример реализации этой функции.
  
## <a name="see-also"></a>См. также



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

