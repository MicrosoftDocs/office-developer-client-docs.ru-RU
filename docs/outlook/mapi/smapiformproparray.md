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
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579314"
---
# <a name="smapiformproparray"></a><span data-ttu-id="f3ca3-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f3ca3-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="f3ca3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3ca3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3ca3-105">Содержит массив структур [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ca3-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3ca3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3ca3-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="f3ca3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f3ca3-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f3ca3-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f3ca3-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="f3ca3-110">Members</span><span class="sxs-lookup"><span data-stu-id="f3ca3-110">Members</span></span>

 <span data-ttu-id="f3ca3-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-111">**cProps**</span></span>
  
> <span data-ttu-id="f3ca3-112">Число именованных свойств в массиве элементов **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="f3ca3-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="f3ca3-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-113">**ulPad**</span></span>
  
>  <span data-ttu-id="f3ca3-114">Восемь байт внутренние поля, используемый для обеспечения правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="f3ca3-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-115">**aFormProp**</span></span>
  
> <span data-ttu-id="f3ca3-116">Массив, содержащий свойства формы.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3ca3-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3ca3-117">Remarks</span></span>

<span data-ttu-id="f3ca3-118">Структура **SMAPIFormPropArray** передается как параметр следующих методов:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="f3ca3-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f3ca3-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="f3ca3-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f3ca3-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="f3ca3-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f3ca3-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="f3ca3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f3ca3-122">See also</span></span>



[<span data-ttu-id="f3ca3-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f3ca3-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="f3ca3-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="f3ca3-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="f3ca3-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f3ca3-125">MAPI Structures</span></span>](mapi-structures.md)

