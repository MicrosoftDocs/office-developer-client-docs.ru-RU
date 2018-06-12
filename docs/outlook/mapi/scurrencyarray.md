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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812228"
---
# <a name="scurrencyarray"></a><span data-ttu-id="3a322-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="3a322-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="3a322-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a322-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a322-105">Содержит массив значений валюты, которые используются для описания свойства типа PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="3a322-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a322-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3a322-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a322-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a322-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="3a322-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="3a322-108">Members</span></span>

 <span data-ttu-id="3a322-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3a322-109">**cValues**</span></span>
  
> <span data-ttu-id="3a322-110">Число значений в массиве, на который указывает член **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="3a322-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="3a322-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="3a322-111">**lpcur**</span></span>
  
> <span data-ttu-id="3a322-112">Указатель на массив структур [валюты](currency.md) , которые содержат денежными значениями.</span><span class="sxs-lookup"><span data-stu-id="3a322-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a322-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a322-113">Remarks</span></span>

<span data-ttu-id="3a322-114">Сведения о PT_MV_CURRENCY содержатся [Типы списка свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3a322-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a322-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3a322-115">See also</span></span>



[<span data-ttu-id="3a322-116">ВАЛЮТА</span><span class="sxs-lookup"><span data-stu-id="3a322-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="3a322-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3a322-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3a322-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3a322-118">MAPI Structures</span></span>](mapi-structures.md)

