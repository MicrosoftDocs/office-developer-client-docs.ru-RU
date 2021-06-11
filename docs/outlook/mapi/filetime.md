---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409505"
---
# <a name="filetime"></a><span data-ttu-id="1aad2-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="1aad2-103">FILETIME</span></span>

  
  
<span data-ttu-id="1aad2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1aad2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1aad2-105">Содержит неподписаное 64-битное значение даты и времени для файла.</span><span class="sxs-lookup"><span data-stu-id="1aad2-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="1aad2-106">Это значение представляет число 100-наносекундных единиц с начала 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="1aad2-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1aad2-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1aad2-107">Header file:</span></span>  <br/> |<span data-ttu-id="1aad2-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1aad2-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="1aad2-109">"Участники"</span><span class="sxs-lookup"><span data-stu-id="1aad2-109">Members</span></span>

 <span data-ttu-id="1aad2-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="1aad2-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="1aad2-111">Низкий заказ 32 бита значения времени файла.</span><span class="sxs-lookup"><span data-stu-id="1aad2-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="1aad2-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="1aad2-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="1aad2-113">32 бита 32 бита значения времени файла.</span><span class="sxs-lookup"><span data-stu-id="1aad2-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aad2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1aad2-114">Remarks</span></span>

<span data-ttu-id="1aad2-115">Свойство типа PT_SYSTIME имеет структуру **FILETIME** для его значения.</span><span class="sxs-lookup"><span data-stu-id="1aad2-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="1aad2-116">Такое свойство имеет тип **данных FILETIME** для участника **Value** в его определении в [структуре SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="1aad2-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="1aad2-117">Определение структуры **FILETIME** находится в справочнике  _программиста Win32_ и в файле mapidefs.h загона MAPI.</span><span class="sxs-lookup"><span data-stu-id="1aad2-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="1aad2-118">MAPI определяет структуру условно, чтобы убедиться, что она определяется, когда определение Win32 недоступно.</span><span class="sxs-lookup"><span data-stu-id="1aad2-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1aad2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1aad2-119">See also</span></span>



[<span data-ttu-id="1aad2-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1aad2-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1aad2-121">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1aad2-121">MAPI Structures</span></span>](mapi-structures.md)

