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
# <a name="smapiforminfoarray"></a><span data-ttu-id="45497-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="45497-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="45497-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45497-105">Содержит массив указателей для формирования объектов сведений.</span><span class="sxs-lookup"><span data-stu-id="45497-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45497-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="45497-106">Header file:</span></span>  <br/> |<span data-ttu-id="45497-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="45497-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="45497-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="45497-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="45497-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="45497-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="45497-110">Members</span><span class="sxs-lookup"><span data-stu-id="45497-110">Members</span></span>

 <span data-ttu-id="45497-111">**Кформс**</span><span class="sxs-lookup"><span data-stu-id="45497-111">**cForms**</span></span>
  
> <span data-ttu-id="45497-112">Количество указателей в массиве, на которые указывает элемент **аформинфо** .</span><span class="sxs-lookup"><span data-stu-id="45497-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="45497-113">**Аформинфо**</span><span class="sxs-lookup"><span data-stu-id="45497-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="45497-114">Указатель на массив указателей для формирования информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="45497-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45497-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="45497-115">Remarks</span></span>

<span data-ttu-id="45497-116">Структура **смапиформинфоаррай** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="45497-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="45497-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="45497-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="45497-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="45497-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="45497-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="45497-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="45497-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="45497-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="45497-121">См. также</span><span class="sxs-lookup"><span data-stu-id="45497-121">See also</span></span>



[<span data-ttu-id="45497-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="45497-122">MAPI Structures</span></span>](mapi-structures.md)

