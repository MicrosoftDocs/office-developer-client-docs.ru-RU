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
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="ac1a9-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="ac1a9-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="ac1a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac1a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac1a9-105">Добавляет одно или несколько свойств типа PT_OBJECT объекту.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ac1a9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac1a9-106">Parameters</span></span>

 <span data-ttu-id="ac1a9-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ac1a9-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="ac1a9-108">[in] Указатель на массив тегов свойств, которые указывают свойства для добавления.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="ac1a9-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="ac1a9-109">_lppProblems_</span></span>
  
> <span data-ttu-id="ac1a9-110">[in, out] При вводе допустимый указатель на [структуру SPropProblemArray](spropproblemarray.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="ac1a9-111">На выходе указатель на указатель на структуру, содержаную сведения о свойствах, которые нельзя добавить, или NULL.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="ac1a9-112">Указатель на структуру массива проблем свойств возвращается только в том случае, если допустимый указатель передается.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac1a9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac1a9-113">Return value</span></span>

<span data-ttu-id="ac1a9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac1a9-114">S_OK</span></span> 
  
> <span data-ttu-id="ac1a9-115">Свойства успешно добавлены.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="ac1a9-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac1a9-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="ac1a9-117">Тип свойства, помимо PT_OBJECT, был передан в массиве, на который указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="ac1a9-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="ac1a9-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac1a9-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ac1a9-119">Установлено, что объект не разрешает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="ac1a9-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ac1a9-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ac1a9-121">Некоторые, но не все свойства были добавлены.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac1a9-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac1a9-122">Remarks</span></span>

<span data-ttu-id="ac1a9-123">Метод **IPropData::HrAddObjProps** добавляет одно или несколько свойств типа PT_OBJECT объекту.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="ac1a9-124">**HrAddObjProps** предоставляет альтернативу методу [IMAPIProp::SetProps](imapiprop-setprops.md) для свойств объектов, так как свойства объектов невозможно создать с помощью вызова **SetProps.**</span><span class="sxs-lookup"><span data-stu-id="ac1a9-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="ac1a9-125">Добавление свойства объекта приводит к включению тега свойств в список тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="ac1a9-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac1a9-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ac1a9-126">Notes to callers</span></span>

<span data-ttu-id="ac1a9-127">Если **hrAddObjProps** возвращает MAPI_W_PARTIAL_COMPLETION и вы задали  _lppProblems_ допустимый указатель, проверьте возвращенную структуру [SPropProblemArray,](spropproblemarray.md) чтобы узнать, какие свойства не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="ac1a9-128">Как правило, единственная проблема, которая возникает, это отсутствие памяти.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="ac1a9-129">Освободите **структуру SPropProblemArray,** назвав функцию [MAPIFreeBuffer](mapifreebuffer.md) после ее завершения.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="ac1a9-130">Чтобы добавить свойство, целевой объект должен иметь разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="ac1a9-131">Если **hrAddObjProps** возвращает MAPI_E_NO_ACCESS, нельзя добавлять свойства к объекту, так как он не разрешает изменения.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="ac1a9-132">Чтобы получить разрешение на чтение и записи объекта перед вызовом **HrAddObjProps,** позвоните по телефону [IPropData::HrSetObjAccess и](ipropdata-hrsetobjaccess.md) установите параметр  _ulAccess_ в IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac1a9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ac1a9-133">See also</span></span>



[<span data-ttu-id="ac1a9-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac1a9-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac1a9-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ac1a9-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="ac1a9-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ac1a9-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ac1a9-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac1a9-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

