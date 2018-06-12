---
title: Многопоточность и управление памятью
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807308"
---
# <a name="multithreading-and-memory-management"></a>Многопоточность и управление памятью

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Правильность обработки памяти является важной создание надежных надстроек XLL для Microsoft Excel. Сбой, связанный с выделения буферов памяти соответствующие и освободить их, если они больше не требуются снижает производительность, создает вероятность конфликта ресурсов и нестабильно работает Excel.
  
Приступая к работе с Microsoft Office Excel 2007, вы можете настроить Excel для использования до 1024 параллельных потоков при перерасчете. В некоторых случаях особенно в том случае, когда доступно множество процессоров или с помощью пользовательских функций, работающим на серверах кластера Многопоточность может повысить производительность.
  
В следующих разделах рассматриваются способы управления памяти и потоков в XLL-модулей:
  
- [���������� ������� � Excel](memory-management-in-excel.md)
    
- [��������������� � ��������� ������ � Excel](multithreading-and-memory-contention-in-excel.md)
    
- [�������������� �������� � Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>См. также



[���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)

