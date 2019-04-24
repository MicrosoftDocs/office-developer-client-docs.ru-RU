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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309515"
---
# <a name="smapiformproparray"></a><span data-ttu-id="f0f71-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f0f71-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="f0f71-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0f71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0f71-105">Содержит массив структур [смапиформпроп](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="f0f71-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0f71-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f0f71-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0f71-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="f0f71-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f0f71-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="f0f71-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f0f71-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f0f71-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="f0f71-110">Members</span><span class="sxs-lookup"><span data-stu-id="f0f71-110">Members</span></span>

 <span data-ttu-id="f0f71-111">**Кпропс**</span><span class="sxs-lookup"><span data-stu-id="f0f71-111">**cProps**</span></span>
  
> <span data-ttu-id="f0f71-112">Количество именованных свойств в массиве элемента **аформпроп** .</span><span class="sxs-lookup"><span data-stu-id="f0f71-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="f0f71-113">**Улпад**</span><span class="sxs-lookup"><span data-stu-id="f0f71-113">**ulPad**</span></span>
  
>  <span data-ttu-id="f0f71-114">Восемь байтов заполнения, используемых для обеспечения правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="f0f71-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="f0f71-115">**Аформпроп**</span><span class="sxs-lookup"><span data-stu-id="f0f71-115">**aFormProp**</span></span>
  
> <span data-ttu-id="f0f71-116">Массив свойств формы.</span><span class="sxs-lookup"><span data-stu-id="f0f71-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0f71-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0f71-117">Remarks</span></span>

<span data-ttu-id="f0f71-118">Структура **смапиформпропаррай** передается в качестве параметра следующим методам:</span><span class="sxs-lookup"><span data-stu-id="f0f71-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="f0f71-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f0f71-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="f0f71-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f0f71-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="f0f71-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="f0f71-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="f0f71-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f0f71-122">See also</span></span>



[<span data-ttu-id="f0f71-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="f0f71-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="f0f71-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="f0f71-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="f0f71-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f71-125">MAPI Structures</span></span>](mapi-structures.md)

