---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585572"
---
# <a name="sguidarray"></a><span data-ttu-id="7b462-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="7b462-103">SGuidArray</span></span>

  
  
<span data-ttu-id="7b462-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b462-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b462-105">Содержит массив структур [идентификатор GUID](guid.md) , используемые для описания свойства типа PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="7b462-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b462-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7b462-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b462-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b462-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="7b462-108">Members</span><span class="sxs-lookup"><span data-stu-id="7b462-108">Members</span></span>

 <span data-ttu-id="7b462-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7b462-109">**cValues**</span></span>
  
> <span data-ttu-id="7b462-110">Число значений в массиве, на который указывает член **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="7b462-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="7b462-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="7b462-111">**lpguid**</span></span>
  
> <span data-ttu-id="7b462-112">Указатель на массив структур **идентификатор GUID** , который содержит значения идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="7b462-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7b462-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b462-113">Remarks</span></span>

<span data-ttu-id="7b462-114">Дополнительные сведения о PT_MV_CLSID увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7b462-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b462-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7b462-115">See also</span></span>



[<span data-ttu-id="7b462-116">ИДЕНТИФИКАТОР GUID</span><span class="sxs-lookup"><span data-stu-id="7b462-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="7b462-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7b462-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7b462-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7b462-118">MAPI Structures</span></span>](mapi-structures.md)

