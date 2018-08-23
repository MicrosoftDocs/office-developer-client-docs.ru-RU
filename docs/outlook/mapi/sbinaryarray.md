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
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586468"
---
# <a name="sbinaryarray"></a><span data-ttu-id="59ddb-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="59ddb-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="59ddb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59ddb-105">Содержит массив двоичных значений.</span><span class="sxs-lookup"><span data-stu-id="59ddb-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59ddb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="59ddb-106">Header file:</span></span>  <br/> |<span data-ttu-id="59ddb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59ddb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="59ddb-108">Members</span><span class="sxs-lookup"><span data-stu-id="59ddb-108">Members</span></span>

 <span data-ttu-id="59ddb-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="59ddb-109">**cValues**</span></span>
  
> <span data-ttu-id="59ddb-110">Число значений в массиве, на который указывает член **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="59ddb-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="59ddb-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="59ddb-111">**lpbin**</span></span>
  
> <span data-ttu-id="59ddb-112">Указатель на массив структур [SBinary](sbinary.md) , в котором содержатся двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="59ddb-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59ddb-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="59ddb-113">Remarks</span></span>

<span data-ttu-id="59ddb-114">Структура **SBinaryArray** используется для описания свойств типа PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="59ddb-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="59ddb-115">Дополнительные сведения о PT_MV_BINARY увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="59ddb-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59ddb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="59ddb-116">See also</span></span>



[<span data-ttu-id="59ddb-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="59ddb-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="59ddb-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="59ddb-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="59ddb-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="59ddb-119">MAPI Structures</span></span>](mapi-structures.md)

