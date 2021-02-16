---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439270"
---
# <a name="sdoublearray"></a><span data-ttu-id="c3838-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="c3838-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="c3838-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3838-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3838-105">Содержит массив doubles, используемый для описания свойства типа PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="c3838-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3838-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c3838-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3838-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3838-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="c3838-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="c3838-108">Members</span></span>

 <span data-ttu-id="c3838-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c3838-109">**cValues**</span></span>
  
> <span data-ttu-id="c3838-110">Количество значений в массиве, на который указывает **член lpdbl.**</span><span class="sxs-lookup"><span data-stu-id="c3838-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="c3838-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="c3838-111">**lpdbl**</span></span>
  
> <span data-ttu-id="c3838-112">Указатель на массив двойных значений.</span><span class="sxs-lookup"><span data-stu-id="c3838-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3838-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3838-113">Remarks</span></span>

<span data-ttu-id="c3838-114">Дополнительные сведения о PT_MV_DOUBLE [см. в списке типов свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="c3838-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3838-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c3838-115">See also</span></span>



[<span data-ttu-id="c3838-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c3838-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c3838-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c3838-117">MAPI Structures</span></span>](mapi-structures.md)

