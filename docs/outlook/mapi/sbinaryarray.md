---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438290"
---
# <a name="sbinaryarray"></a><span data-ttu-id="61efb-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="61efb-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="61efb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61efb-105">Содержит массив двоичных значений.</span><span class="sxs-lookup"><span data-stu-id="61efb-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61efb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="61efb-106">Header file:</span></span>  <br/> |<span data-ttu-id="61efb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61efb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="61efb-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="61efb-108">Members</span></span>

 <span data-ttu-id="61efb-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="61efb-109">**cValues**</span></span>
  
> <span data-ttu-id="61efb-110">Количество значений в массиве, на который указывает член **lpbin.**</span><span class="sxs-lookup"><span data-stu-id="61efb-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="61efb-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="61efb-111">**lpbin**</span></span>
  
> <span data-ttu-id="61efb-112">Указатель на массив [структур SBinary,](sbinary.md) которые удерживают двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="61efb-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="61efb-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="61efb-113">Remarks</span></span>

<span data-ttu-id="61efb-114">Структура **SBinaryArray** используется для описания свойств типа PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="61efb-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="61efb-115">Дополнительные сведения о PT_MV_BINARY см. [в списке типов свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="61efb-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61efb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="61efb-116">See also</span></span>



[<span data-ttu-id="61efb-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="61efb-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="61efb-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="61efb-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="61efb-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="61efb-119">MAPI Structures</span></span>](mapi-structures.md)

