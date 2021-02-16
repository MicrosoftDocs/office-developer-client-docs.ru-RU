---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331390"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="e2cab-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="e2cab-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="e2cab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2cab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2cab-105">Содержит массив [LARGE_INTEGER,](https://go.microsoft.com/fwlink/?LinkId=132130) используемых для описания свойства типа PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="e2cab-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cab-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e2cab-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2cab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2cab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="e2cab-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e2cab-108">Members</span></span>

 <span data-ttu-id="e2cab-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e2cab-109">**cValues**</span></span>
  
> <span data-ttu-id="e2cab-110">Количество значений в массиве, на который указывает **член lpli.**</span><span class="sxs-lookup"><span data-stu-id="e2cab-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="e2cab-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="e2cab-111">**lpli**</span></span>
  
> <span data-ttu-id="e2cab-112">Указатель на массив **LARGE_INTEGER,** которые удерживают целый ряд значений.</span><span class="sxs-lookup"><span data-stu-id="e2cab-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2cab-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2cab-113">Remarks</span></span>

<span data-ttu-id="e2cab-114">Дополнительные сведения о PT_MV_18 [см. в списке типов свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="e2cab-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2cab-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e2cab-115">See also</span></span>



[<span data-ttu-id="e2cab-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e2cab-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e2cab-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cab-117">MAPI Structures</span></span>](mapi-structures.md)

