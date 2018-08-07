---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6389bbf2094f51711d80896db0db9862059826cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812341"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="e8992-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="e8992-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="e8992-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e8992-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e8992-105">Содержит набор ссылок на объекты формы.</span><span class="sxs-lookup"><span data-stu-id="e8992-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8992-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e8992-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8992-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e8992-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e8992-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="e8992-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e8992-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="e8992-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="e8992-110">Members</span><span class="sxs-lookup"><span data-stu-id="e8992-110">Members</span></span>

 <span data-ttu-id="e8992-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="e8992-111">**cForms**</span></span>
  
> <span data-ttu-id="e8992-112">Число указатели массива, на который указывает член **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="e8992-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="e8992-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="e8992-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="e8992-114">Указатель на массив ссылок на объекты формы.</span><span class="sxs-lookup"><span data-stu-id="e8992-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8992-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8992-115">Remarks</span></span>

<span data-ttu-id="e8992-116">Структура **SMAPIFormInfoArray** передается как параметр в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="e8992-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="e8992-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e8992-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="e8992-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="e8992-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="e8992-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="e8992-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="e8992-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e8992-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="e8992-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e8992-121">See also</span></span>



[<span data-ttu-id="e8992-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e8992-122">MAPI Structures</span></span>](mapi-structures.md)

