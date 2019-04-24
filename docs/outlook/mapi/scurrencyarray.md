---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360699"
---
# <a name="scurrencyarray"></a><span data-ttu-id="706cf-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="706cf-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="706cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="706cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="706cf-105">Содержит массив значений денежных единиц, которые используются для описания свойства типа ПТ_МВ_КУРРЕНЦИ.</span><span class="sxs-lookup"><span data-stu-id="706cf-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="706cf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="706cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="706cf-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="706cf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="706cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="706cf-108">Members</span></span>

 <span data-ttu-id="706cf-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="706cf-109">**cValues**</span></span>
  
> <span data-ttu-id="706cf-110">Количество значений в массиве, на которое указывает элемент **лпкур** .</span><span class="sxs-lookup"><span data-stu-id="706cf-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="706cf-111">**лпкур**</span><span class="sxs-lookup"><span data-stu-id="706cf-111">**lpcur**</span></span>
  
> <span data-ttu-id="706cf-112">Указатель на массив структур [валюты](currency.md) , который содержит значения денежных единиц.</span><span class="sxs-lookup"><span data-stu-id="706cf-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="706cf-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="706cf-113">Remarks</span></span>

<span data-ttu-id="706cf-114">Сведения о ПТ_МВ_КУРРЕНЦИ приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="706cf-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="706cf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="706cf-115">See also</span></span>



[<span data-ttu-id="706cf-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="706cf-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="706cf-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="706cf-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="706cf-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="706cf-118">MAPI Structures</span></span>](mapi-structures.md)

