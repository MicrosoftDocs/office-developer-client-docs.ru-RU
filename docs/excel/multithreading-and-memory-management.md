---
title: Многопоточность и управление памятью
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310390"
---
# <a name="multithreading-and-memory-management"></a>Многопоточность и управление памятью

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Правильная обработка памяти крайне важна для создания надежных надстроек XLL для Microsoft Excel. Не удается выделить соответствующие буферы памяти и освободить их, когда они больше не нужны, уменьшает производительность, создает состязание за ресурсы и дестабилизации Excel.
  
Начиная с Microsoft Office Excel 2007, вы можете настроить Excel для использования до 1 024 параллельных потоков при пересчете. В некоторых случаях, особенно при наличии нескольких процессоров или с пользовательскими функциями, работающими на кластерных серверах, многопоточность может увеличить производительность.
  
В следующих разделах описано, как управлять памятью и потоками в XLL:
  
- [Управление памятью в Excel](memory-management-in-excel.md)
    
- [��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Многопоточный пересчет в Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>См. также



[Разработка XLL-файлов для Excel](developing-excel-xlls.md)

