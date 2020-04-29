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
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424926"
---
# <a name="sguidarray"></a><span data-ttu-id="a8abf-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="a8abf-103">SGuidArray</span></span>

  
  
<span data-ttu-id="a8abf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8abf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8abf-105">Содержит массив структуры [GUID](guid.md) , который используется для описания свойства типа PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="a8abf-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8abf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8abf-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8abf-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a8abf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="a8abf-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a8abf-108">Members</span></span>

 <span data-ttu-id="a8abf-109">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="a8abf-109">**cValues**</span></span>
  
> <span data-ttu-id="a8abf-110">Количество значений в массиве, на которое указывает элемент **лпгуид** .</span><span class="sxs-lookup"><span data-stu-id="a8abf-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="a8abf-111">**лпгуид**</span><span class="sxs-lookup"><span data-stu-id="a8abf-111">**lpguid**</span></span>
  
> <span data-ttu-id="a8abf-112">Указатель на массив структур **GUID** , который содержит значения идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="a8abf-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8abf-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8abf-113">Remarks</span></span>

<span data-ttu-id="a8abf-114">Дополнительные сведения о PT_MV_CLSID приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="a8abf-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8abf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a8abf-115">See also</span></span>



[<span data-ttu-id="a8abf-116">GUID</span><span class="sxs-lookup"><span data-stu-id="a8abf-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a8abf-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a8abf-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a8abf-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a8abf-118">MAPI Structures</span></span>](mapi-structures.md)

