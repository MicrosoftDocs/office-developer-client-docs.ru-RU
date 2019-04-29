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
# <a name="sbinaryarray"></a><span data-ttu-id="39266-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="39266-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="39266-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39266-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39266-105">Содержит массив двоичных значений.</span><span class="sxs-lookup"><span data-stu-id="39266-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39266-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="39266-106">Header file:</span></span>  <br/> |<span data-ttu-id="39266-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="39266-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="39266-108">Members</span><span class="sxs-lookup"><span data-stu-id="39266-108">Members</span></span>

 <span data-ttu-id="39266-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="39266-109">**cValues**</span></span>
  
> <span data-ttu-id="39266-110">Количество значений в массиве, на которое указывает элемент **лпбин** .</span><span class="sxs-lookup"><span data-stu-id="39266-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="39266-111">**лпбин**</span><span class="sxs-lookup"><span data-stu-id="39266-111">**lpbin**</span></span>
  
> <span data-ttu-id="39266-112">Указатель на массив структур [сбинари](sbinary.md) , в котором хранятся двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="39266-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39266-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="39266-113">Remarks</span></span>

<span data-ttu-id="39266-114">Структура **сбинаряррай** используется для описания свойств типа пт_мв_бинари.</span><span class="sxs-lookup"><span data-stu-id="39266-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="39266-115">Дополнительные сведения о ПТ_МВ_БИНАРИ приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="39266-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39266-116">См. также</span><span class="sxs-lookup"><span data-stu-id="39266-116">See also</span></span>



[<span data-ttu-id="39266-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="39266-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="39266-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="39266-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="39266-119">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="39266-119">MAPI Structures</span></span>](mapi-structures.md)

