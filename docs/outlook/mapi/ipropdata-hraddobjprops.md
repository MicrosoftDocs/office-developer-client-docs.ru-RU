---
title: ипропдатахраддобжпропс
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
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="f9124-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="f9124-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="f9124-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9124-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9124-105">Добавляет одно или несколько свойств типа PT_OBJECT в объект.</span><span class="sxs-lookup"><span data-stu-id="f9124-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="f9124-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9124-106">Parameters</span></span>

 <span data-ttu-id="f9124-107">_лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="f9124-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="f9124-108">возврата Указатель на массив тегов свойств, указывающий свойства, которые требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="f9124-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="f9124-109">_лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="f9124-109">_lppProblems_</span></span>
  
> <span data-ttu-id="f9124-110">[вход, выход] На входе, допустимый указатель на структуру [спроппроблемаррай](spropproblemarray.md) или значение null.</span><span class="sxs-lookup"><span data-stu-id="f9124-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="f9124-111">В выходных данных указатель на указатель на структуру, содержащую сведения о свойствах, которые не удалось добавить, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f9124-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="f9124-112">Указатель на структуру массива неполадок свойств возвращается только в том случае, если передается допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="f9124-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f9124-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9124-113">Return value</span></span>

<span data-ttu-id="f9124-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9124-114">S_OK</span></span> 
  
> <span data-ttu-id="f9124-115">Свойства успешно добавлены.</span><span class="sxs-lookup"><span data-stu-id="f9124-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="f9124-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="f9124-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="f9124-117">В массиве, на который указывает параметр _лппроптагаррай_ , был передан тип свойства, отличный от PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="f9124-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="f9124-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f9124-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f9124-119">Для объекта задано разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f9124-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="f9124-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f9124-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f9124-121">Некоторые (но не все) свойства были добавлены.</span><span class="sxs-lookup"><span data-stu-id="f9124-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9124-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9124-122">Remarks</span></span>

<span data-ttu-id="f9124-123">Метод **ипропдата:: храддобжпропс** добавляет одно или несколько свойств типа PT_OBJECT в объект.</span><span class="sxs-lookup"><span data-stu-id="f9124-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="f9124-124">**Храддобжпропс** предоставляет альтернативу методу [IMAPIProp:: SetProps](imapiprop-setprops.md) для свойств объекта, так как свойства объекта невозможно создать с помощью метода **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="f9124-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="f9124-125">При добавлении свойства объекта в тег свойства включается в список тегов свойств, возвращаемых методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="f9124-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9124-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f9124-126">Notes to callers</span></span>

<span data-ttu-id="f9124-127">Если **храддобжпропс** возвращает MAPI_W_PARTIAL_COMPLETION и вы настроили _лпппроблемс_ на допустимый указатель, Проверьте возвращаемую структуру [спроппроблемаррай](spropproblemarray.md) , чтобы узнать, какие свойства не были добавлены.</span><span class="sxs-lookup"><span data-stu-id="f9124-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="f9124-128">Как правило, единственная неполадка связана с нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="f9124-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="f9124-129">Освободите структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) по завершении работы с ней.</span><span class="sxs-lookup"><span data-stu-id="f9124-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="f9124-130">Для добавления свойства целевой объект должен иметь разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f9124-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="f9124-131">Если **храддобжпропс** возвращает MAPI_E_NO_ACCESS, невозможно добавить свойства для объекта, так как он не разрешает изменение.</span><span class="sxs-lookup"><span data-stu-id="f9124-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="f9124-132">Чтобы получить разрешение на чтение и запись объекта перед вызовом **храддобжпропс**, вызовите [Ипропдата:: хрсетобжакцесс](ipropdata-hrsetobjaccess.md) и присвойте параметру _улакцесс_ значение IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="f9124-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9124-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f9124-133">See also</span></span>



[<span data-ttu-id="f9124-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9124-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f9124-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f9124-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="f9124-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f9124-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f9124-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f9124-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

