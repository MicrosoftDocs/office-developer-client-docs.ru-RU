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
# <a name="filetime"></a><span data-ttu-id="bd6a5-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="bd6a5-103">FILETIME</span></span>

  
  
<span data-ttu-id="bd6a5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd6a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd6a5-105">Содержит Неподписанное 64 – разрядное значение даты и времени для файла.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="bd6a5-106">Это значение представляет число единиц 100 НС с начала 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd6a5-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bd6a5-107">Header file:</span></span>  <br/> |<span data-ttu-id="bd6a5-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bd6a5-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="bd6a5-109">Members</span><span class="sxs-lookup"><span data-stu-id="bd6a5-109">Members</span></span>

 <span data-ttu-id="bd6a5-110">**Двловдатетиме**</span><span class="sxs-lookup"><span data-stu-id="bd6a5-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="bd6a5-111">Младшие биты 32 значения времени файла.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="bd6a5-112">**Двхигхдатетиме**</span><span class="sxs-lookup"><span data-stu-id="bd6a5-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="bd6a5-113">32 бит высокого порядка бит значения времени файла.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd6a5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd6a5-114">Remarks</span></span>

<span data-ttu-id="bd6a5-115">Свойство типа ПТ_СИСТИМЕ имеет структуру **fileTime** для его значения.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="bd6a5-116">Такое свойство имеет тип данных **fileTime** для элемента **value** в его определении в структуре [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="bd6a5-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="bd6a5-117">Определение структуры **fileTime** находится в справочнике программиста _Win32_ и в файле заголовка MAPI MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="bd6a5-118">MAPI определяет структуру условно, чтобы убедиться, что она определена, когда определение Win32 недоступно.</span><span class="sxs-lookup"><span data-stu-id="bd6a5-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd6a5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bd6a5-119">See also</span></span>



[<span data-ttu-id="bd6a5-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bd6a5-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bd6a5-121">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bd6a5-121">MAPI Structures</span></span>](mapi-structures.md)

