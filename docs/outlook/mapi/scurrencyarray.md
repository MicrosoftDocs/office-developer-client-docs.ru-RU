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
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812228"
---
# <a name="scurrencyarray"></a><span data-ttu-id="bbcdd-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="bbcdd-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="bbcdd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbcdd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbcdd-105">Содержит массив значений валюты, которые используются для описания свойства типа PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="bbcdd-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbcdd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bbcdd-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbcdd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbcdd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="bbcdd-108">Members</span><span class="sxs-lookup"><span data-stu-id="bbcdd-108">Members</span></span>

 <span data-ttu-id="bbcdd-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bbcdd-109">**cValues**</span></span>
  
> <span data-ttu-id="bbcdd-110">Число значений в массиве, на который указывает член **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="bbcdd-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="bbcdd-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="bbcdd-111">**lpcur**</span></span>
  
> <span data-ttu-id="bbcdd-112">Указатель на массив структур [валюты](currency.md) , которые содержат денежными значениями.</span><span class="sxs-lookup"><span data-stu-id="bbcdd-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bbcdd-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbcdd-113">Remarks</span></span>

<span data-ttu-id="bbcdd-114">Сведения о PT_MV_CURRENCY содержатся [Типы списка свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="bbcdd-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbcdd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bbcdd-115">See also</span></span>



[<span data-ttu-id="bbcdd-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="bbcdd-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="bbcdd-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bbcdd-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bbcdd-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bbcdd-118">MAPI Structures</span></span>](mapi-structures.md)

