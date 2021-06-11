---
title: Управление многочитаниями и памятью
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414468"
---
# <a name="multithreading-and-memory-management"></a>Управление многочитаниями и памятью

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Правильная обработка памяти имеет жизненно важное значение для создания надежных надстройок XLL для Microsoft Excel. Неспособность выделить соответствующие буферы памяти и освободить их, когда они больше не нужны, снижает производительность, создает раздор ресурсов и Excel.
  
Начиная с Microsoft Office Excel 2007 г. можно настроить Excel для использования до 1024 одновременно потоков при пересчете. В некоторых случаях, особенно при наличии нескольких процессоров или с пользовательскими функциями, работающими на кластерных серверах, многочитание может повысить производительность.
  
Ниже описаны вопросы управления памятью и потоками в XLLs:
  
- [Управление памятью в Excel](memory-management-in-excel.md)
    
- [��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Многопоточный пересчет в Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>См. также



[Разработка XLL-файлов для Excel](developing-excel-xlls.md)

