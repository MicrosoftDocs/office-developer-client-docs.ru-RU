---
title: Справочник по функциям API SDK XLL для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Справочник по функциям API [Excel 2007], функции [Excel 2007], справочник [Excel 2007], пакет средств разработки XLL для Excel 2007, справочник
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715958"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Справочник по функциям API SDK XLL для Excel

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пакет SDK XLL для Microsoft Excel 2013 содержит исходные файлы для библиотеки платформы, предназначенной для ускорения записи библиотек XLL, а также два примера проектов (Example и Generic). 
  
В этом разделе приведены справочные сведения по следующим функциям:
  
- обратные вызовы Excel, доступные для XLL;
    
- обратные вызовы XLL, поиск которых выполняется в Microsoft Excel;
    
- ключевые функции в примерах проектов и платформ.
    
## <a name="sample-projects"></a>Примеры проектов

Пакет SDK XLL для Excel 2013 содержит исходные файлы и файлы проектов Microsoft Visual Studio для следующих примеров проектов:
  
- Проект **Framework** (`SAMPLES\FRAMEWRK\`) содержит проект, который можно встроить в библиотеку FRAMEWRK.lib для последующего связывания с другими проектами XLL. Эта библиотека включает множество функций и инструментов, которые упрощают написание библиотек XLL. Данная библиотека используется в каждом из других проектов в сочетании с файлом заголовка FRAMEWRK.h.
    
- Проект **Example** (`SAMPLES\EXAMPLE\`) содержит проект EXAMPLE.xll, который можно встроить в библиотеку XLL. Библиотека XLL включает ряд примеров использования библиотеки платформы, а также пример реализации функций интерфейса надстройки XLL, таких как **xlAutoOpen**.
    
- Проект **Generic** (`SAMPLES\GENERIC\`) содержит проект GENERIC.xll, который можно встроить в библиотеку XLL. Эта библиотека XLL демонстрирует несколько примеров функций и команд. Ее можно использовать в качестве отправной точки при написании собственных библиотек XLL.
    
## <a name="in-this-section"></a>В этом разделе

- [Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Функции обратного вызова API C: Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)
  
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Функции в библиотеке платформы](functions-in-the-framework-library.md)
  
- [Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)
  
- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Дополнительные ресурсы

- [Программирование с использованием API C в Excel](programming-with-the-c-api-in-excel.md)
  
- [Разработка библиотек XLL для Excel](developing-excel-xlls.md)

