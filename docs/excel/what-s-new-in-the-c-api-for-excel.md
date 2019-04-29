---
title: Новые возможности API C для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c API [Excel 2007], новые возможности
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
  
В сочетании с Microsoft Excel 2013 пакет средств разработки программного обеспечения (SDK) Microsoft Excel 2013 XLL включает поддержку следующих функций.
  
- **Новые функции**
    
    ПАКЕТ SDK XLL для Microsoft Excel 2013 поддерживает обратное обращение ко всем новым функциям листа в Excel 2013. Дополнительные сведения о вызове функций Excel 2013 см. в статье [вызов Excel из библиотеки DLL или XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Асинхронные пользовательские функции**
    
    Excel 2013 поддерживает асинхронный вызов пользовательских функций (UDF), что может увеличить производительность, одновременно разрешив выполнение нескольких вычислений. Дополнительные сведения об асинхронных пользовательских функциях можно найти в статье [асинхронНые пользовательские функции](asynchronous-user-defined-functions.md).
    
- **Соединители кластера**
    
    Соединители кластера позволяют выполнять функции UDF на высокопроизводительных вычислительных кластерах. Дополнительные сведения о создании соединителей кластера содержатся в разделе [Разработка кластерНых соединителЕй Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Надстройки XLL, которые вы планируете запускать в вычислительных кластерах, должны вызывать только функции, безопасные кластером. Для получения дополнительных сведений о функциях, которые можно использовать, ознакомьтесь со статьей [Справка по функциям API пакета SDK для Office XLL](excel-xll-sdk-api-function-reference.md) и [безопасные функции кластера](cluster-safe-functions.md). 
  
- **Поддержка 64 бит**
    
    Теперь вы можете скомпилировать и связать как 32, так и 64 – битовые XLL. Дополнительную информацию можно узнать в статье [Создание XLL](creating-xlls.md).
    
## <a name="see-also"></a>См. также



[Разработка XLL-файлов для Excel](developing-excel-xlls.md)
  
[Программирование с использованием API C в Excel](programming-with-the-c-api-in-excel.md)
  
[��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)


[Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

