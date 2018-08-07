---
title: Использование относительного времени для доступа к данным о доступности
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Интерфейс IFreeBusyData в интерфейсе API доступности использует концепцию относительное время — это число минут, начиная с 1 января 1601, выраженная в время в формате UTC, и является значение типа LONG.
ms.openlocfilehash: b83cd46cfcc4d84d4fc3bf000dd8b0acdda545dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807700"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Использование относительного времени для доступа к данным о доступности

Интерфейс [IFreeBusyData](ifreebusydata.md) в интерфейсе API доступности использует концепцию относительное время — это число минут, начиная с 1 января 1601, выраженная в время в формате UTC и является значение типа **LONG**. 
  
Ниже приведены некоторые часто используемые относительно времени значения.
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Следуйте предыдущего значения максимально и минимально относительно времени для убедитесь, что необходимые значения относительно времени.
  
Так как NTFS изначально записывает время файлов в формате [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , может быть удобным для использования в следующем примере кода для преобразования относительно времени в **FILETIME**. 
  
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

- [About the Free/Busy API](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

