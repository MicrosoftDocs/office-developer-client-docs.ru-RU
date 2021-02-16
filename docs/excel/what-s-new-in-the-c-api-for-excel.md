---
title: Новые возможности API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- C api [excel 2007], что нового
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
# <a name="whats-new-in-the-c-api-for-excel"></a>Новые возможности API C для Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
В сочетании с Microsoft Excel 2013 пакет средств разработки программного обеспечения XLL для Microsoft Excel 2013 (SDK) включает поддержку следующих функций.
  
- **Новые функции**
    
    Microsoft Excel 2013 XLL SDK поддерживает вызов всех новых функций листа в Excel 2013. Дополнительные сведения о вызове функций Excel [](calling-into-excel-from-the-dll-or-xll.md)2013 см. в этой теме.
    
- **Асинхронные пользовательские функции**
    
    Excel 2013 поддерживает асинхронный вызов пользовательских функций (UDF), что может повысить производительность, позволяя выполнять несколько вычислений одновременно. Дополнительные сведения об асинхронных функцияхudf см. в [User-Defined.](asynchronous-user-defined-functions.md)
    
- **Соединители кластера**
    
    Соединители кластера позволяют использовать UDF в высокопроводительных вычислительных кластерах. Дополнительные сведения о создании соединитеителей кластера см. в [подключении к разработке соединители кластера Excel.](developing-excel-cluster-connectors.md)
    
    > [!NOTE]
    > Надстройки XLL, которые вы собираетесь запускать в вычислительных кластерах, должны вызывать только функции, безопасные для кластеров. Дополнительные сведения о функциях, которые можно использовать, см. в справочнике по [функциям API SDK для Excel и](excel-xll-sdk-api-function-reference.md) в справочнике по функциям [кластера.](cluster-safe-functions.md) 
  
- **64-битная поддержка**
    
    Теперь можно скомпилировать и связать 32- и 64-битные XLL. Дополнительные сведения см. [в теме "Создание XLL".](creating-xlls.md)
    
## <a name="see-also"></a>См. также



[Разработка XLL-файлов для Excel](developing-excel-xlls.md)
  
[Программирование с использованием API C в Excel](programming-with-the-c-api-in-excel.md)
  
[��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)


[Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

