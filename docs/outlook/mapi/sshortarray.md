---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812387"
---
# <a name="sshortarray"></a><span data-ttu-id="591a6-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="591a6-103">SShortArray</span></span>

  
  
<span data-ttu-id="591a6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="591a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="591a6-105">Содержит массив целых значений, которые используются для описания свойства типа PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="591a6-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="591a6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="591a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="591a6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="591a6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="591a6-108">Members</span><span class="sxs-lookup"><span data-stu-id="591a6-108">Members</span></span>

 <span data-ttu-id="591a6-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="591a6-109">**cValues**</span></span>
  
> <span data-ttu-id="591a6-110">Число значений в массиве, на который указывает член **строки** .</span><span class="sxs-lookup"><span data-stu-id="591a6-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="591a6-111">**линий на дюйм**</span><span class="sxs-lookup"><span data-stu-id="591a6-111">**lpi**</span></span>
  
> <span data-ttu-id="591a6-112">Указатель на массив целых значений.</span><span class="sxs-lookup"><span data-stu-id="591a6-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="591a6-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="591a6-113">Remarks</span></span>

<span data-ttu-id="591a6-114">Дополнительные сведения о PT_MV_SHORT и других типов свойств можно [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="591a6-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="591a6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="591a6-115">See also</span></span>



[<span data-ttu-id="591a6-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="591a6-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="591a6-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="591a6-117">MAPI Structures</span></span>](mapi-structures.md)

