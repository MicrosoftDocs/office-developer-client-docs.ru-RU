---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420068"
---
# <a name="smapiformproparray"></a><span data-ttu-id="9479d-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9479d-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="9479d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9479d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9479d-105">Содержит массив структур [SMAPIFormProp.](smapiformprop.md)</span><span class="sxs-lookup"><span data-stu-id="9479d-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9479d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9479d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9479d-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="9479d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9479d-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="9479d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9479d-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9479d-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="9479d-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="9479d-110">Members</span></span>

 <span data-ttu-id="9479d-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="9479d-111">**cProps**</span></span>
  
> <span data-ttu-id="9479d-112">Количество именуемых свойств в массиве **в члене aFormProp.**</span><span class="sxs-lookup"><span data-stu-id="9479d-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="9479d-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="9479d-113">**ulPad**</span></span>
  
>  <span data-ttu-id="9479d-114">Восемь байт заполнения, используемого для обеспечения правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="9479d-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="9479d-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="9479d-115">**aFormProp**</span></span>
  
> <span data-ttu-id="9479d-116">Массив свойств формы.</span><span class="sxs-lookup"><span data-stu-id="9479d-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9479d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="9479d-117">Remarks</span></span>

<span data-ttu-id="9479d-118">Структура **SMAPIFormPropArray** передается в качестве параметра следующим методам:</span><span class="sxs-lookup"><span data-stu-id="9479d-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="9479d-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9479d-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="9479d-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9479d-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="9479d-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9479d-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="9479d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9479d-122">See also</span></span>



[<span data-ttu-id="9479d-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9479d-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="9479d-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="9479d-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="9479d-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9479d-125">MAPI Structures</span></span>](mapi-structures.md)

