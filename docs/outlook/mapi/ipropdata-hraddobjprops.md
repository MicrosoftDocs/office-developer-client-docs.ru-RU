---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416386"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="e4111-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="e4111-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="e4111-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4111-105">Добавляет одно или несколько свойств типа PT_OBJECT в объект.</span><span class="sxs-lookup"><span data-stu-id="e4111-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="e4111-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4111-106">Parameters</span></span>

 <span data-ttu-id="e4111-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e4111-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e4111-108">[in] Указатель на массив тегов свойств, которые указывают свойства, которые необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="e4111-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="e4111-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="e4111-109">_lppProblems_</span></span>
  
> <span data-ttu-id="e4111-110">[in, out] При вводе допустимый указатель на [структуру SPropProblemArray](spropproblemarray.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="e4111-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="e4111-111">При выходе указатель на структуру, которая содержит сведения о свойствах, которые не удалось добавить, или NULL.</span><span class="sxs-lookup"><span data-stu-id="e4111-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="e4111-112">Указатель на структуру массива проблем свойств возвращается, только если передается допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="e4111-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4111-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4111-113">Return value</span></span>

<span data-ttu-id="e4111-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4111-114">S_OK</span></span> 
  
> <span data-ttu-id="e4111-115">Свойства успешно добавлены.</span><span class="sxs-lookup"><span data-stu-id="e4111-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="e4111-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="e4111-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="e4111-117">Тип свойства, не PT_OBJECT был передан в массив, на который указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="e4111-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="e4111-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e4111-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e4111-119">В объекте не разрешается разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="e4111-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="e4111-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="e4111-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="e4111-121">Некоторые (но не все) свойства были добавлены.</span><span class="sxs-lookup"><span data-stu-id="e4111-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4111-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4111-122">Remarks</span></span>

<span data-ttu-id="e4111-123">Метод **IPropData::HrAddObjProps** добавляет одно или несколько свойств типа PT_OBJECT объекту.</span><span class="sxs-lookup"><span data-stu-id="e4111-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="e4111-124">**HrAddObjProps** предоставляет альтернативу методу [IMAPIProp::SetProps](imapiprop-setprops.md) для свойств объекта, так как свойства объекта невозможно создать путем вызова **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="e4111-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="e4111-125">Добавление свойства объекта приводит к включению тега свойства в список тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="e4111-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e4111-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e4111-126">Notes to callers</span></span>

<span data-ttu-id="e4111-127">Если **HrAddObjProps** возвращает MAPI_W_PARTIAL_COMPLETION и для  _lppProblems_ установлен допустимый указатель, проверьте возвращенную структуру [SPropProblemArray,](spropproblemarray.md) чтобы узнать, какие свойства не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="e4111-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="e4111-128">Обычно единственная проблема заключается в нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="e4111-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="e4111-129">Освободите **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer](mapifreebuffer.md) по ее завершению.</span><span class="sxs-lookup"><span data-stu-id="e4111-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="e4111-130">Чтобы добавить свойство, целевой объект должен иметь разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="e4111-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="e4111-131">Если **HrAddObjProps** возвращает MAPI_E_NO_ACCESS, вы не можете добавить свойства в объект, так как он не допускает изменения.</span><span class="sxs-lookup"><span data-stu-id="e4111-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="e4111-132">Чтобы получить разрешение на чтение и записи для объекта перед вызовом **HrAddObjProps,** вызовите [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) и задайте для параметра  _ulAccess_ значение IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="e4111-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4111-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e4111-133">See also</span></span>



[<span data-ttu-id="e4111-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e4111-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e4111-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e4111-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="e4111-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e4111-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e4111-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e4111-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

