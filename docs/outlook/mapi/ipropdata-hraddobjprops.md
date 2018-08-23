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
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591688"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="c6d8b-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="c6d8b-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="c6d8b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6d8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6d8b-105">Добавление одного или нескольких свойств типа PT_OBJECT объект.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="c6d8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6d8b-106">Parameters</span></span>

 <span data-ttu-id="c6d8b-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c6d8b-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c6d8b-108">[in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="c6d8b-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="c6d8b-109">_lppProblems_</span></span>
  
> <span data-ttu-id="c6d8b-110">[in, out] На вводимых пользователем данных, допустимый указатель на структуру [SPropProblemArray](spropproblemarray.md) , или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="c6d8b-111">В выходных данных, указатель указатель на структуру, которая содержит сведения о свойствах, которые не могут быть добавлены или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="c6d8b-112">Указатель на структуру массива проблема свойство возвращается только в том случае, если передается указатель допустимый.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6d8b-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c6d8b-113">Return value</span></span>

<span data-ttu-id="c6d8b-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c6d8b-114">S_OK</span></span> 
  
> <span data-ttu-id="c6d8b-115">Свойства были успешно добавлены.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="c6d8b-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="c6d8b-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="c6d8b-117">Свойство введите, отличное от PT_OBJECT был передан в массиве, параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="c6d8b-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="c6d8b-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c6d8b-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c6d8b-119">Объект имеет значение не разрешать разрешение на чтение/запись.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="c6d8b-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c6d8b-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c6d8b-121">Некоторые, но не для всех свойств были добавлены.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6d8b-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6d8b-122">Remarks</span></span>

<span data-ttu-id="c6d8b-123">Метод **IPropData::HrAddObjProps** добавляет одного или нескольких свойств типа PT_OBJECT к объекту.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="c6d8b-124">**HrAddObjProps** является альтернативой метод [IMAPIProp::SetProps](imapiprop-setprops.md) для свойства объекта, так как свойства объекта не могут создаваться путем вызова **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="c6d8b-125">Добавление свойства объекта результаты в тег свойства, в списке свойство теги, метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) возвращает.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6d8b-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c6d8b-126">Notes to callers</span></span>

<span data-ttu-id="c6d8b-127">Если **HrAddObjProps** возвращает MAPI_W_PARTIAL_COMPLETION и установки _lppProblems_ допустимый указатель, проверяет, возвращенные структура [SPropProblemArray](spropproblemarray.md) для получения свойств, которые не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="c6d8b-128">Как правило только проблемы, возникающей — нехватка памяти.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="c6d8b-129">Бесплатная загрузка структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) , когда вы закончите с ним.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="c6d8b-130">Чтобы добавить свойство, целевой объект должен иметь разрешение на чтение/запись.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="c6d8b-131">Если **HrAddObjProps** возвращает MAPI_E_NO_ACCESS, так как он не позволяет изменять свойства нельзя добавить объект.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="c6d8b-132">Чтобы получить разрешение на чтение и запись в объект до вызова **HrAddObjProps**, вызовите [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) и установите для параметра _ulAccess_ значение IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6d8b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c6d8b-133">See also</span></span>



[<span data-ttu-id="c6d8b-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c6d8b-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c6d8b-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c6d8b-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="c6d8b-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c6d8b-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c6d8b-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c6d8b-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

