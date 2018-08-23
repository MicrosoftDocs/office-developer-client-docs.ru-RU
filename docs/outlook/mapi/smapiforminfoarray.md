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
ms.openlocfilehash: 6c09c271fefcf31dcde01526d65091714c0b682d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576276"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="5ea6c-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="5ea6c-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="5ea6c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ea6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ea6c-105">Содержит набор ссылок на объекты формы.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ea6c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5ea6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ea6c-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="5ea6c-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5ea6c-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="5ea6c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5ea6c-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="5ea6c-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="5ea6c-110">Members</span><span class="sxs-lookup"><span data-stu-id="5ea6c-110">Members</span></span>

 <span data-ttu-id="5ea6c-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="5ea6c-111">**cForms**</span></span>
  
> <span data-ttu-id="5ea6c-112">Число указатели массива, на который указывает член **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="5ea6c-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="5ea6c-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="5ea6c-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="5ea6c-114">Указатель на массив ссылок на объекты формы.</span><span class="sxs-lookup"><span data-stu-id="5ea6c-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ea6c-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ea6c-115">Remarks</span></span>

<span data-ttu-id="5ea6c-116">Структура **SMAPIFormInfoArray** передается как параметр в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="5ea6c-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="5ea6c-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5ea6c-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="5ea6c-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="5ea6c-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="5ea6c-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="5ea6c-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="5ea6c-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5ea6c-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="5ea6c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5ea6c-121">See also</span></span>



[<span data-ttu-id="5ea6c-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5ea6c-122">MAPI Structures</span></span>](mapi-structures.md)

