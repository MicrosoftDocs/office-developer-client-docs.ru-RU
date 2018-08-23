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
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577424"
---
# <a name="sbinary"></a><span data-ttu-id="8e495-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="8e495-103">SBinary</span></span>

  
  
<span data-ttu-id="8e495-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e495-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e495-105">Описывает свойства типа PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="8e495-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e495-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8e495-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e495-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e495-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="8e495-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e495-108">Members</span></span>

 <span data-ttu-id="8e495-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="8e495-109">**cb**</span></span>
  
> <span data-ttu-id="8e495-110">Число байт в элемент **lpb** .</span><span class="sxs-lookup"><span data-stu-id="8e495-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="8e495-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="8e495-111">**lpb**</span></span>
  
> <span data-ttu-id="8e495-112">Указатель на значение свойства PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="8e495-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e495-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e495-113">Remarks</span></span>

<span data-ttu-id="8e495-114">Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e495-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e495-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8e495-115">See also</span></span>



[<span data-ttu-id="8e495-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e495-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8e495-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8e495-117">MAPI Structures</span></span>](mapi-structures.md)

