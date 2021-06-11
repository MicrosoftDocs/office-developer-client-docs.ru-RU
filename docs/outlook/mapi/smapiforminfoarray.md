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
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416974"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="96137-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="96137-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="96137-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96137-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96137-105">Содержит массив указателей для формирования информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="96137-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96137-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="96137-106">Header file:</span></span>  <br/> |<span data-ttu-id="96137-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="96137-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="96137-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="96137-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="96137-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="96137-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="96137-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="96137-110">Members</span></span>

 <span data-ttu-id="96137-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="96137-111">**cForms**</span></span>
  
> <span data-ttu-id="96137-112">Количество указателей в массиве, на который указывает **член aFormInfo.**</span><span class="sxs-lookup"><span data-stu-id="96137-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="96137-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="96137-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="96137-114">Указатель на массив указателей для формирования информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="96137-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96137-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="96137-115">Remarks</span></span>

<span data-ttu-id="96137-116">Структура **SMAPIFormInfoArray** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="96137-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="96137-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="96137-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="96137-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="96137-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="96137-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="96137-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="96137-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="96137-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="96137-121">См. также</span><span class="sxs-lookup"><span data-stu-id="96137-121">See also</span></span>



[<span data-ttu-id="96137-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="96137-122">MAPI Structures</span></span>](mapi-structures.md)

