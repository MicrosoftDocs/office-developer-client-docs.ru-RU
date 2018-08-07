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
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808440"
---
# <a name="filetime"></a><span data-ttu-id="996b5-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="996b5-103">FILETIME</span></span>

  
  
<span data-ttu-id="996b5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="996b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="996b5-105">Содержит неподписанные 64-разрядная версия значения даты и времени для файла.</span><span class="sxs-lookup"><span data-stu-id="996b5-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="996b5-106">Это значение представляет число единиц 100 наносекунд с момента запуска 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="996b5-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="996b5-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="996b5-107">Header file:</span></span>  <br/> |<span data-ttu-id="996b5-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="996b5-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="996b5-109">Members</span><span class="sxs-lookup"><span data-stu-id="996b5-109">Members</span></span>

 <span data-ttu-id="996b5-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="996b5-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="996b5-111">Младшие 32 разряда значение времени, в файл.</span><span class="sxs-lookup"><span data-stu-id="996b5-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="996b5-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="996b5-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="996b5-113">Старшие 32 разряда значение времени, в файл.</span><span class="sxs-lookup"><span data-stu-id="996b5-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="996b5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="996b5-114">Remarks</span></span>

<span data-ttu-id="996b5-115">Свойство типа PT_SYSTIME имеет структуру **FILETIME** его значение.</span><span class="sxs-lookup"><span data-stu-id="996b5-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="996b5-116">Такое свойство имеет тип данных **FILETIME** для элемента **значение** в его определение в структуре [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="996b5-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="996b5-117">Определение структуры **FILETIME** происходит в _Справочник программиста Win32_ в файл заголовка MAPI Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="996b5-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="996b5-118">MAPI определяет структуру условию, убедитесь в том, что оно указано при определении Win32 недоступен.</span><span class="sxs-lookup"><span data-stu-id="996b5-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="996b5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="996b5-119">See also</span></span>



[<span data-ttu-id="996b5-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="996b5-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="996b5-121">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="996b5-121">MAPI Structures</span></span>](mapi-structures.md)

