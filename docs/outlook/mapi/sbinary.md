---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812176"
---
# <a name="sbinary"></a><span data-ttu-id="1e804-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="1e804-103">SBinary</span></span>

  
  
<span data-ttu-id="1e804-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e804-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e804-105">Описывает свойства типа PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="1e804-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e804-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1e804-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e804-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e804-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="1e804-108">Members</span><span class="sxs-lookup"><span data-stu-id="1e804-108">Members</span></span>

 <span data-ttu-id="1e804-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="1e804-109">**cb**</span></span>
  
> <span data-ttu-id="1e804-110">Число байт в элемент **lpb** .</span><span class="sxs-lookup"><span data-stu-id="1e804-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="1e804-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="1e804-111">**lpb**</span></span>
  
> <span data-ttu-id="1e804-112">Указатель на значение свойства PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="1e804-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e804-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e804-113">Remarks</span></span>

<span data-ttu-id="1e804-114">Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1e804-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e804-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1e804-115">See also</span></span>



[<span data-ttu-id="1e804-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1e804-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1e804-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1e804-117">MAPI Structures</span></span>](mapi-structures.md)

