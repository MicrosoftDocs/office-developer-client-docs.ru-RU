---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407776"
---
# <a name="spropproblem"></a><span data-ttu-id="aca5b-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="aca5b-103">SPropProblem</span></span>

  
  
<span data-ttu-id="aca5b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aca5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aca5b-105">В этой статье описывается ошибка, связанная с операцией, включающей в себя свойство.</span><span class="sxs-lookup"><span data-stu-id="aca5b-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aca5b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="aca5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="aca5b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="aca5b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="aca5b-108">Members</span><span class="sxs-lookup"><span data-stu-id="aca5b-108">Members</span></span>

 <span data-ttu-id="aca5b-109">**Улиндекс**</span><span class="sxs-lookup"><span data-stu-id="aca5b-109">**ulIndex**</span></span>
  
> <span data-ttu-id="aca5b-110">Индекс в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="aca5b-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="aca5b-111">**Улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="aca5b-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="aca5b-112">Тег Property для свойства с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="aca5b-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="aca5b-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="aca5b-113">**scode**</span></span>
  
> <span data-ttu-id="aca5b-114">Значение ошибки, описывающее проблему со свойством.</span><span class="sxs-lookup"><span data-stu-id="aca5b-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="aca5b-115">Это значение может быть любым значением [SCODE](scode.md) MAPI.</span><span class="sxs-lookup"><span data-stu-id="aca5b-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aca5b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="aca5b-116">Remarks</span></span>

<span data-ttu-id="aca5b-117">Массив структур **спроппроблем** возвращается из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="aca5b-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="aca5b-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="aca5b-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="aca5b-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="aca5b-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="aca5b-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="aca5b-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="aca5b-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="aca5b-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="aca5b-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="aca5b-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="aca5b-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="aca5b-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="aca5b-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="aca5b-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="aca5b-125">Структура **спроппроблем** содержит значение ошибки **SCODE** , полученное в результате операции, пытающейся изменить или удалить свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="aca5b-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="aca5b-126">Дополнительные сведения о том, как структура **спроппроблем** работает с ошибками, связанными со свойствами, в разделе [свойства MAPI с именем](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="aca5b-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aca5b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="aca5b-127">See also</span></span>



[<span data-ttu-id="aca5b-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="aca5b-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="aca5b-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="aca5b-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="aca5b-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="aca5b-130">MAPI Structures</span></span>](mapi-structures.md)

