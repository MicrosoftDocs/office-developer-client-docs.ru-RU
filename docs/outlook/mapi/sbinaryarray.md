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
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812179"
---
# <a name="sbinaryarray"></a><span data-ttu-id="a0266-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="a0266-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="a0266-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0266-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0266-105">Содержит массив двоичных значений.</span><span class="sxs-lookup"><span data-stu-id="a0266-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0266-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a0266-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0266-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0266-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="a0266-108">Members</span><span class="sxs-lookup"><span data-stu-id="a0266-108">Members</span></span>

 <span data-ttu-id="a0266-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a0266-109">**cValues**</span></span>
  
> <span data-ttu-id="a0266-110">Число значений в массиве, на который указывает член **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="a0266-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="a0266-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="a0266-111">**lpbin**</span></span>
  
> <span data-ttu-id="a0266-112">Указатель на массив структур [SBinary](sbinary.md) , в котором содержатся двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="a0266-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0266-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0266-113">Remarks</span></span>

<span data-ttu-id="a0266-114">Структура **SBinaryArray** используется для описания свойств типа PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="a0266-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="a0266-115">Дополнительные сведения о PT_MV_BINARY увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="a0266-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0266-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a0266-116">See also</span></span>



[<span data-ttu-id="a0266-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="a0266-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="a0266-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a0266-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a0266-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a0266-119">MAPI Structures</span></span>](mapi-structures.md)

