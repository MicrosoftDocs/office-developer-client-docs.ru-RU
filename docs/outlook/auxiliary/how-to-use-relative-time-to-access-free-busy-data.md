---
title: Использование относительного времени для доступа к данным о занятости
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Интерфейс Ифрибусидата в API сведений о доступности использует концепцию относительного времени, которая представляет собой количество минут с 1 января 1601, выраженное в универсальном времени (UTC), и является значением типа LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317635"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Использование относительного времени для доступа к данным о занятости

Интерфейс [ифрибусидата](ifreebusydata.md) в API сведений о доступности использует концепцию относительного времени, которая представляет собой количество минут с 1 января 1601, выраженное в универсальном времени (UTC), и является значением типа **Long**. 
  
Ниже приведены некоторые из часто используемых относительных значений времени.
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Используйте предыдущие значения максимального и минимального времени для проверки допустимости относительных значений времени.
  
Так как файлы NTFS записываются в формате [fileTime](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , можно использовать следующий пример кода для преобразования относительного времени в значение **fileTime**и обратно. 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

