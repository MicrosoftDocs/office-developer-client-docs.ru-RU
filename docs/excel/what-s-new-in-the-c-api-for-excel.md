---
title: Что нового в API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [Excel 2007], новые возможности
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439690"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Что нового в API C для Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вместе с Microsoft Excel 2013, Microsoft Excel 2013 XLL Software Development Kit (SDK) включает поддержку следующих функций.
  
- **Новые функции**
    
    В Microsoft Excel 2013 XLL SDK поддерживается вызов всех новых функций таблицы в Excel 2013 г. Дополнительные сведения о вызове Excel 2013 г. см. в Excel в DLL или [XLL.](calling-into-excel-from-the-dll-or-xll.md)
    
- **Асинхронные функции, определенные пользователем**
    
    Excel 2013 г. поддерживает асинхронный вызов определенных пользователем функций (UDF), что может повысить производительность, позволяя выполнять несколько вычислений одновременно. Дополнительные сведения об асинхронных UDFs см. в User-Defined [Functions.](asynchronous-user-defined-functions.md)
    
- **Соединители кластера**
    
    Соединители кластера позволяют UDF-системам работать на высокопродувных вычислительных кластерах. Дополнительные сведения о создании соединители кластеров см. в [Excel.](developing-excel-cluster-connectors.md)
    
    > [!NOTE]
    > Надстройки XLL, которые вы собираетесь запускать в вычислительных кластерах, должны вызывать только функции, безопасные для кластеров. Дополнительные сведения о функциях, которые можно использовать, см. в Excel [XLL SDK API Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Сейф Functions.](cluster-safe-functions.md) 
  
- **64-битная поддержка**
    
    Теперь можно скомпилировать и связать 32-битные и 64-битные XLLs. Дополнительные сведения см. в [дополнительных сведениях о создании XLLs.](creating-xlls.md)
    
## <a name="see-also"></a>См. также



[Разработка XLL-файлов для Excel](developing-excel-xlls.md)
  
[Программирование с использованием API C в Excel](programming-with-the-c-api-in-excel.md)
  
[��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)


[Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

