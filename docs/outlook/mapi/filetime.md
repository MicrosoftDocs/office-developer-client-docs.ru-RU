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
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583255"
---
# <a name="filetime"></a><span data-ttu-id="6b529-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="6b529-103">FILETIME</span></span>

  
  
<span data-ttu-id="6b529-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b529-105">Содержит неподписанные 64-разрядная версия значения даты и времени для файла.</span><span class="sxs-lookup"><span data-stu-id="6b529-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="6b529-106">Это значение представляет число единиц 100 наносекунд с момента запуска 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="6b529-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b529-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6b529-107">Header file:</span></span>  <br/> |<span data-ttu-id="6b529-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b529-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="6b529-109">Members</span><span class="sxs-lookup"><span data-stu-id="6b529-109">Members</span></span>

 <span data-ttu-id="6b529-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="6b529-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="6b529-111">Младшие 32 разряда значение времени, в файл.</span><span class="sxs-lookup"><span data-stu-id="6b529-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="6b529-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="6b529-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="6b529-113">Старшие 32 разряда значение времени, в файл.</span><span class="sxs-lookup"><span data-stu-id="6b529-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b529-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6b529-114">Remarks</span></span>

<span data-ttu-id="6b529-115">Свойство типа PT_SYSTIME имеет структуру **FILETIME** его значение.</span><span class="sxs-lookup"><span data-stu-id="6b529-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="6b529-116">Такое свойство имеет тип данных **FILETIME** для элемента **значение** в его определение в структуре [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6b529-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="6b529-117">Определение структуры **FILETIME** происходит в _Справочник программиста Win32_ в файл заголовка MAPI Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="6b529-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="6b529-118">MAPI определяет структуру условию, убедитесь в том, что оно указано при определении Win32 недоступен.</span><span class="sxs-lookup"><span data-stu-id="6b529-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b529-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6b529-119">See also</span></span>



[<span data-ttu-id="6b529-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b529-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6b529-121">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6b529-121">MAPI Structures</span></span>](mapi-structures.md)

