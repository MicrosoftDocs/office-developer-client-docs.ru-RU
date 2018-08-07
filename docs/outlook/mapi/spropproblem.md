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
ms.openlocfilehash: 32aa91d43e4674c0de20a0dbb670dcb9e2c782cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812357"
---
# <a name="spropproblem"></a><span data-ttu-id="23e21-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="23e21-103">SPropProblem</span></span>

  
  
<span data-ttu-id="23e21-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23e21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23e21-105">Содержит описание ошибки, которые относятся к операции, включающие использование свойства.</span><span class="sxs-lookup"><span data-stu-id="23e21-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23e21-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="23e21-106">Header file:</span></span>  <br/> |<span data-ttu-id="23e21-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23e21-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="23e21-108">Members</span><span class="sxs-lookup"><span data-stu-id="23e21-108">Members</span></span>

 <span data-ttu-id="23e21-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="23e21-109">**ulIndex**</span></span>
  
> <span data-ttu-id="23e21-110">Индекс массива тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="23e21-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="23e21-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="23e21-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="23e21-112">Тег свойства для свойства, которое содержит ошибки.</span><span class="sxs-lookup"><span data-stu-id="23e21-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="23e21-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="23e21-113">**scode**</span></span>
  
> <span data-ttu-id="23e21-114">Значение ошибки, описанием проблемы со свойством.</span><span class="sxs-lookup"><span data-stu-id="23e21-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="23e21-115">Это значение может быть любое значение MAPI [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="23e21-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="23e21-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="23e21-116">Remarks</span></span>

<span data-ttu-id="23e21-117">Массив структур **SPropProblem** возвращается из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="23e21-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="23e21-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="23e21-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="23e21-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="23e21-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="23e21-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="23e21-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="23e21-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="23e21-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="23e21-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="23e21-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="23e21-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="23e21-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="23e21-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="23e21-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="23e21-125">Структура **SPropProblem** содержит значение **SCODE** ошибки, результатом операции, изменение или удаление свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="23e21-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="23e21-126">Дополнительные сведения о работе структура **SPropProblem** при этом возникают ошибки, связанные с свойства в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="23e21-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23e21-127">См. также</span><span class="sxs-lookup"><span data-stu-id="23e21-127">See also</span></span>



[<span data-ttu-id="23e21-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="23e21-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="23e21-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="23e21-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="23e21-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="23e21-130">MAPI Structures</span></span>](mapi-structures.md)

