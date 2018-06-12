---
title: Справочник по функции API пакет SDK XLL для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Справочник по функциям API [excel 2007], [Excel 2007] функции, ссылки [Excel 2007, Excel 2007 XLL пакет средств разработки, ссылка
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807251"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Справочник по функции API пакет SDK XLL для Excel

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пакет SDK Microsoft Excel 2013 XLL содержит исходные файлы для библиотеки Framework, предназначенный для ускорения записи XLL-модулей и два примера проекта, пример и универсальный. 
  
В этом разделе представлены ссылки на функцию для следующих:
  
- Обратные вызовы для Excel, которые могут вызывать XLL.
    
- XLL обратных вызовов, которые ищет Microsoft Excel.
    
- Ключевые функции в проектах образец и framework.
    
## <a name="sample-projects"></a>Примеры проектов

Пакет SDK Excel XLL 2013 предоставляет исходные файлы и файлы проекта Microsoft Visual Studio для следующие примеры проектов:
  
- Проект **Framework** (`SAMPLES\FRAMEWRK\`) содержит проекта, который можно создать в библиотеке FRAMEWRK.lib, который затем могут быть связаны в другие проекты XLL. Библиотека содержит множество функций и средств, которые делают создание XLL-модулей для удобства. Эта библиотека используется в обоих других проектов в сочетании с файл заголовка FRAMEWRK.h.
    
- **Пример** проекта (`SAMPLES\EXAMPLE\`) содержит проекта, который можно создать в надстройке XLL EXAMPLE.xll. Многие примеры использования библиотеки Framework и примеры реализации функции интерфейса надстройки XLL, такие как **xlAutoOpen**XLL.
    
- **Универсальный** проекта (`SAMPLES\GENERIC\`) содержит проекта, который можно создать в надстройке XLL GENERIC.xll. XLL демонстрирует несколько пример функции и команды и является хорошей отправной точкой для написания собственного XLL-модулей.
    
## <a name="in-this-section"></a>В этом разделе

- [Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)
  
- [������� ��������� ������ API C Excel4 Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)
  
- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Функции в библиотеке Framework](functions-in-the-framework-library.md)
  
- [В универсальные библиотеки DLL](functions-in-the-generic-dll.md)
  
- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>См. также

- [���������������� � �������������� C API � Excel](programming-with-the-c-api-in-excel.md)
  
- [���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)

