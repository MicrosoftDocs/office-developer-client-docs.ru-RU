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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812333"
---
# <a name="smapiformproparray"></a><span data-ttu-id="996e9-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="996e9-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="996e9-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="996e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="996e9-105">Содержит массив структур [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="996e9-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="996e9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="996e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="996e9-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="996e9-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="996e9-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="996e9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="996e9-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="996e9-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="996e9-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="996e9-110">Members</span></span>

 <span data-ttu-id="996e9-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="996e9-111">**cProps**</span></span>
  
> <span data-ttu-id="996e9-112">Число именованных свойств в массиве элементов **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="996e9-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="996e9-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="996e9-113">**ulPad**</span></span>
  
>  <span data-ttu-id="996e9-114">Восемь байт внутренние поля, используемый для обеспечения правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="996e9-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="996e9-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="996e9-115">**aFormProp**</span></span>
  
> <span data-ttu-id="996e9-116">Массив, содержащий свойства формы.</span><span class="sxs-lookup"><span data-stu-id="996e9-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="996e9-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="996e9-117">Remarks</span></span>

<span data-ttu-id="996e9-118">Структура **SMAPIFormPropArray** передается как параметр следующих методов:</span><span class="sxs-lookup"><span data-stu-id="996e9-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="996e9-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="996e9-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="996e9-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="996e9-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="996e9-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="996e9-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="996e9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="996e9-122">See also</span></span>



[<span data-ttu-id="996e9-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="996e9-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="996e9-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="996e9-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="996e9-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="996e9-125">MAPI Structures</span></span>](mapi-structures.md)

