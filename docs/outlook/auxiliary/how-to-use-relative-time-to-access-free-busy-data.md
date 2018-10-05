---
title: Использование относительного времени для доступа к данным о доступности
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Интерфейс IFreeBusyData в интерфейсе API доступности использует концепцию относительное время — это число минут, начиная с 1 января 1601, выраженная в время в формате UTC, и является значение типа LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386938"
---
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="07763-103">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="07763-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="07763-104">Интерфейс [IFreeBusyData](ifreebusydata.md) в интерфейсе API доступности использует концепцию относительное время — это число минут, начиная с 1 января 1601, выраженная в время в формате UTC и является значение типа **LONG**.</span><span class="sxs-lookup"><span data-stu-id="07763-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="07763-105">Ниже приведены некоторые часто используемые относительно времени значения.</span><span class="sxs-lookup"><span data-stu-id="07763-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="07763-106">Следуйте предыдущего значения максимально и минимально относительно времени для убедитесь, что необходимые значения относительно времени.</span><span class="sxs-lookup"><span data-stu-id="07763-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="07763-107">Так как NTFS изначально записывает время файлов в формате [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , может быть удобным для использования в следующем примере кода для преобразования относительно времени в **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="07763-107">Because NTFS records file times natively in [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="07763-108">См. также</span><span class="sxs-lookup"><span data-stu-id="07763-108">See also</span></span>

- [<span data-ttu-id="07763-109">About the Free/Busy API</span><span class="sxs-lookup"><span data-stu-id="07763-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="07763-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="07763-110">IFreeBusyData</span></span>](ifreebusydata.md)

