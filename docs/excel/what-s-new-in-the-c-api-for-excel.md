---
title: Новые возможности интерфейса API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], новые возможности
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19807325"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Новые возможности интерфейса API C для Excel

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
В сочетании с Microsoft Excel 2013 Microsoft Excel 2013 XLL Software Development Kit (SDK) поддерживает следующие функции.
  
- **Новые функции**
    
    Пакет SDK XLL Microsoft Excel 2013 поддерживает обратного вызова для всех дополнительных функций листов в Excel 2013. Дополнительные сведения о вызове функции Excel 2013 [вызов в Excel из DLL или XLL](calling-into-excel-from-the-dll-or-xll.md)см.
    
- **Асинхронные пользовательские функции**
    
    Excel 2013 поддерживает вызов пользовательских функций (UDF) асинхронно, которой могут улучшить производительность, включив несколько вычислений для запуска в то же время. Дополнительные сведения о асинхронных пользовательских функций [Asynchronous_User-Defined](asynchronous-user-defined-functions.md)см.
    
- **Соединители кластера**
    
    Соединителей кластеров для включения пользовательских функций для запуска на высокопроизводительные вычислительные кластеры. Дополнительные сведения о создании соединителей кластеров можно [Разработка соединителей кластеров для Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Надстройки XLL, которые предполагается запускать на вычислительные кластеры должны вызывать только функции безопасно кластера. Дополнительные сведения о функции можно использовать, [Справочник по функциям Excel XLL SDK API](excel-xll-sdk-api-function-reference.md) и [Безопасные для кластера функции](cluster-safe-functions.md). 
  
- **Поддержка 64-разрядная версия**
    
    Теперь можно скомпилировать и связать 32- и 64-разрядная версия XLL-модулей. Дополнительные сведения содержатся в разделе [Создание XLL-модулей](creating-xlls.md).
    
## <a name="see-also"></a>См. также



[���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)
  
[���������������� � �������������� C API � Excel](programming-with-the-c-api-in-excel.md)
  
[��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)


[��������� � ������ � SDK XLL ��� Excel 2013](getting-started-with-the-excel-xll-sdk.md)

