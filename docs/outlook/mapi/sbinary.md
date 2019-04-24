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
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357521"
---
# <a name="sbinary"></a><span data-ttu-id="051db-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="051db-103">SBinary</span></span>

  
  
<span data-ttu-id="051db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="051db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="051db-105">Описывает свойство типа ПТ_БИНАРИ.</span><span class="sxs-lookup"><span data-stu-id="051db-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="051db-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="051db-106">Header file:</span></span>  <br/> |<span data-ttu-id="051db-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="051db-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="051db-108">Members</span><span class="sxs-lookup"><span data-stu-id="051db-108">Members</span></span>

 <span data-ttu-id="051db-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="051db-109">**cb**</span></span>
  
> <span data-ttu-id="051db-110">Количество байтов в элементе **ЛПБ** .</span><span class="sxs-lookup"><span data-stu-id="051db-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="051db-111">**ЛПБ**</span><span class="sxs-lookup"><span data-stu-id="051db-111">**lpb**</span></span>
  
> <span data-ttu-id="051db-112">Указатель на значение свойства ПТ_БИНАРИ.</span><span class="sxs-lookup"><span data-stu-id="051db-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="051db-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="051db-113">Remarks</span></span>

<span data-ttu-id="051db-114">Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="051db-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="051db-115">См. также</span><span class="sxs-lookup"><span data-stu-id="051db-115">See also</span></span>



[<span data-ttu-id="051db-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="051db-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="051db-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="051db-117">MAPI Structures</span></span>](mapi-structures.md)

